# readme��д�ĵ�example-���ؿɿ�Դ��

[����ת�ص�ַ��](http://www.coderli.com/write-readme-for-your-project/)

## ʵ��һ

Markdown �﷨�ٲ��
1 ���������ָ�ʽ
����
# ���� H1 <һ������>
## ���� H2 <��������>
###### ���� H6 <��������>
���ָ�ʽ
**�������ִ����ʽ**
*��������б���ʽ*
~~�����������ɾ����~~
2 �б�
�����б�
* ��Ŀ1
* ��Ŀ2
* ��Ŀ3
�����б�
1. ��Ŀ1
2. ��Ŀ2
3. ��Ŀ3
   * ��Ŀ1
   * ��Ŀ2
3 ����
ͼƬ
![ͼƬ����](http://gitcafe.com/image.png)
����
[��������](http://gitcafe.com)
����
> ��һ����������
> �ڶ�����������
ˮƽ��
***
����
`<hello world>`
��������
```ruby
  def add(a, b)
    return a + b
  end
```
���
  ��ͷ  | ��ͷ
  ------------- | -------------
 ��Ԫ������  | ��Ԫ������
 ��Ԫ������l  | ��Ԫ������

## ʵ����

![Shurnim icon](http://onecoder.qiniudn.com/8wuliao/DLPii2Jx/rEBO.jpg)

## Ŀ¼
* [��������](#��������)
* [��Ŀ����](#��Ŀ����)
* [ʹ��˵��](#ʹ��˵��)
  * [��ȡ����](#��ȡ����)
  * [�������](#�������)
  * [ʹ��ShurnimStorage�ӿ�](#ʹ��ShurnimStorage�ӿ�)
       * [�ӿڽ���](#�ӿڽ���)
       * [ʹ������](#ʹ������)
* [����](#����)

<a name="��������"></a>
## ��������

*Shurnim*�����Һ�����������������һֻ��������֡�<br/>
*shurnim-storage*����һ�����ʽ�ƴ洢/����ͬ�������ߡ����ڲμ������ƿ��������Ĺ�������Ʋ�������

<a name="��Ŀ����"></a>
## ��Ŀ����

*shurnim-storage* ����Ƴ����Ǹ�����ṩһ���ɷ�����չ���ƴ洢/����ͬ�����ߡ��ֺ�˽ӿں�ǰ��UI���������֡�<br>

����Ŀǰ�����ƴ洢������ϵͳ��������һ��������֧��֧��ĳ�����ض��洢֮���ͬ������**������**��**��ţ�ƴ洢**��ͬ�����ߣ���ʱ������ͬ�����������������Ҫ�µĹ��ߣ����û��������㡣*shurnim-storage*  ����Ϊ�˽�����������Ƶġ�

��*shurnim-storage*�У��û�ʹ�õĹ̶���ͳһ�ĺ�˽ӿڡ��������ƴ洢/����API��֧�������Բ������ʽ����ϵͳ�еġ���ˣ�����û���Ҫһ����**������**��**Dropbox**��ͬ�����ߣ���ֻ��Ҫ��ԭ�л����ϣ�����**Dropbox**�Ĳ��������ʵ�ֻ�ͨ�������ݡ�<br/>

ͬʱ�����ͳһ�ӿڵ����Ҳ���ǵ����濪�������󣬿�ֱ��ͨ������ṩ�Ľӿڿ�������������չ���ܵ��ƴ洢UI���ߡ�<br>

Ŀǰ����������ܵĺ��Ĳ����Ѿ�����������ɡ�ֻ���𲽲����˽ӿںͲ�������ӿڵĶ��弴�ɡ������ڸ���ʱ����������ޣ�UI����û�п���������Ȥ��ͬѧ����һ�ԡ�

<a name="ʹ��˵��"></a>
## ʹ��˵��

<a name="��ȡ����"></a>
### ��ȡ����

* gitcafe��Ŀ��ҳ: <https://gitcafe.com/onecoder/shurnim-storage-for-UPYUN>
* OSChina��Ŀ��ҳ: <http://git.oschina.net/onecoder/shurnim-storage><br>
OSChina�ϵĻ�������¡�

������Ҳ����ͨ��OSChina��Maven���ȡ�����������Լ�����jar����

* maven

     1. ����OSC�ֿ�
   
                    <repositories>
                      <repository>
                           <id>nexus</id>
                           <name>local private nexus</name>
                           <url>http://maven.oschina.net/content/groups/public/</url>
                           <releases>
                                <enabled>true</enabled>
                           </releases>
                           <snapshots>
                                <enabled>false</enabled>
                           </snapshots>
                      </repository>
                 </repositories>

     2. ��������
   
               <dependency>
                 <groupId>com.coderli</groupId>
                 <artifactId>shurnim-storage</artifactId>
                  <version>0.1-alpha</version>
               </dependency>
* Gradle ����Jar

����ĿĿ¼ִ��
   
     gradle jar
   
<a name="�������"></a>
### �������

��*shurnim-storage*�У��������һ��һ��Ļ�ľ������֧���ſ�ܵĹ��ܣ�Ҳ�ǿ�ܿ���չ�ԵĻ�ʯ������һ�����������������

1. ʵ��PluginAPI�ӿ�

```
package com.coderli.shurnim.storage.plugin;

import java.io.File;
import java.util.List;

import com.coderli.shurnim.storage.plugin.model.Resource;

/**
* �����ƴ洢�����Ҫʵ�ֵ�ͨ�ýӿ�
*
* @author OneCoder
* @date 2014��4��22�� ����9:43:41
* @website http://www.coderli.com
*/
public interface PluginAPI {

     /**
      * ��ʼ���ӿ�
      *
      * @author OneCoder
      * @date 2014��5��19�� ����10:47:40
      */
     void init();

     /**
      * ��ȡ����Դ�б�
      *
      * @param parentPath
      * @return
      * @author OneCoder
      * @date 2014��4��24�� ����11:29:14
      */
     List<Resource> getChildResources(String parentPath);

     /**
      * �����ض�����Դ
      *
      * @param parentPath
      *            Ŀ¼·��
      * @param name
      *            ��Դ����
      * @param storePath
      *            ������Դ����·��
      * @return
      * @author OneCoder
      * @date 2014��4��24�� ����11:30:19
      */
     Resource downloadResource(String parentPath, String name, String storePath);

     /**
      * �����ļ���
      *
      * @param path
      *            �ļ���·��
      * @param auto
      *            �Ƿ��Զ�������Ŀ¼
      * @return
      * @author OneCoder
      * @date 2014��5��15�� ����10:10:04
      */
     boolean mkdir(String path, boolean auto);

     /**
      * �ϴ���Դ
      *
      * @param parentPath
      *            ��Ŀ¼·��
      * @param name
      *            ��Դ����
      * @param uploadFile
      *            ���ϴ��ı����ļ�
      * @return
      * @author OneCoder
      * @date 2014��5��15�� ����10:40:13
      */
     boolean uploadResource(String parentPath, String name, File uploadFile);
}
```

Ŀǰ����Ľӿ��б��Ϊͬ����Դ��ƣ������Ҫ֧�ָ������(��ɾ�������ҵ�)������չ�ýӿڶ��塣<br/><br/>
�ӿ��У����еĲ����ͷ���ֵ��Ϊ*shurnim-storage*����ж����ͨ��ģ�͡���ˣ����ڿ��������������Ҫ���ض�SDK�е�ģ��ת���ɽӿ����ṩ��ģ�͡�<br/><br/>
���ʵ����ֻҪ��*shurnim-storage*������ͬһ��classpath����ʹ�á����ȿ���ֱ����Դ�빤���п�����������繤�����ṩ��*upyun*��*qiniu*���һ����Ҳ������Ϊ�������̿��������jar��������ͬһ��classpath�¡�<br/><br/>
*upyun*�������(���ܲ�����):

```  
package com.coderli.shurnim.storage.upyun.plugin;

import java.io.File;
import java.util.List;

import com.coderli.shurnim.storage.plugin.AbstractPluginAPI;
import com.coderli.shurnim.storage.plugin.model.Resource;
import com.coderli.shurnim.storage.plugin.model.Resource.Type;
import com.coderli.shurnim.storage.upyun.api.UpYun;

public class UpYunPlugin extends AbstractPluginAPI {

     private UpYun upyun;
     private String username;
     private String password;
     private String bucketName;

     public UpYun getUpyun() {
          return upyun;
     }

     public void setUpyun(UpYun upyun) {
          this.upyun = upyun;
     }

     public String getUsername() {
          return username;
     }

     public void setUsername(String username) {
          this.username = username;
     }

     public String getPassword() {
          return password;
     }

     public void setPassword(String password) {
          this.password = password;
     }

     public String getBucketName() {
          return bucketName;
     }

     public void setBucketName(String bucketName) {
          this.bucketName = bucketName;
     }

     /*
      * (non-Javadoc)
      *
      * @see
      * com.coderli.shurnim.storage.plugin.PluginAPI#getChildResources(java.lang
      * .String)
      */
     @Override
     public List<Resource> getChildResources(String parentPath) {
          return null;
     }

     /*
      * (non-Javadoc)
      *
      * @see
      * com.coderli.shurnim.storage.plugin.PluginAPI#downloadResource(java.lang
      * .String, java.lang.String, java.lang.String)
      */
     @Override
     public Resource downloadResource(String parentPath, String name,
               String storePath) {
          File storeFile = new File(storePath);
//          if (!storeFile.exists()) {
//               try {
//                    storeFile.createNewFile();
//               } catch (IOException e) {
//                    e.printStackTrace();
//               }
//          }
          String filePath = getFullPath(parentPath, name);
          upyun.readDir("/api");
          if (upyun.readFile(filePath, storeFile)) {
               Resource result = new Resource();
               result.setName(name);
               result.setPath(parentPath);
               result.setType(Type.FILE);
               result.setLocalFile(storeFile);
               return result;
          }
          return null;
     }

     String getFullPath(String parentPath, String name) {
          if (!parentPath.endsWith(File.separator)) {
               parentPath = parentPath + File.separator;
          }
          return parentPath + name;
     }

     /*
      * (non-Javadoc)
      *
      * @see com.coderli.shurnim.storage.plugin.PluginAPI#mkdir(java.lang.String,
      * boolean)
      */
     @Override
     public boolean mkdir(String path, boolean auto) {
          // TODO Auto-generated method stub
          return false;
     }

     /*
      * (non-Javadoc)
      *
      * @see
      * com.coderli.shurnim.storage.plugin.PluginAPI#uploadResource(java.lang
      * .String, java.lang.String, java.io.File)
      */
     @Override
     public boolean uploadResource(String parentPath, String name,
               File uploadFile) {
          // TODO Auto-generated method stub
          return false;
     }

     /*
      * (non-Javadoc)
      *
      * @see com.coderli.shurnim.storage.plugin.AbstractPluginAPI#init()
      */
     @Override
     public void init() {
          upyun = new UpYun(bucketName, username, password);
     }

}
```


2. ��д��������ļ�

```
<?xml version="1.0" encoding="UTF-8"?>
<plugin>
     <id>qiniu</id>
     <name>��ţ�ƴ洢</name>
     <api>
          <className>com.coderli.shurnim.storage.qiniu.QiniuPlugin</className>
          <params>
               <param name="access_key" displayName="ACCESS_KEY">EjREKHI_GFXbQzyrKdVhhXrIRyj3fRC1s9UmZPZO
               </param>
               <param name="secret_key" displayName="SECRET_KEY">88NofFWUvkfJ6T6rGRxlDSZOQxWkIxY2IsFIXJLX
               </param>
               <param name="bucketName" displayName="�ռ���">onecoder
               </param>
          </params>
     </api>
</plugin>
```
   * **id** Ϊ�ò����*shurnim-storage*����µ�Ψһ��ʶ�������ظ������
    * **name** Ϊ��ʾֵ��ΪUI�����ṩ�ɹ���ʾ���������ֵ��
    * **className** Ϊ����ӿ�ʵ���������·��������
    * **params/param** Ϊ�����Ҫ�û����õĲ����б�����
         * *name* �������������Ҫ��ӿ�ʵ�����еĲ������ϸ�һ�£��ұ�������Ӧ��set�����ĸ�ʽҪ���ϸ񣬼�set+����ĸ��д�Ĳ�����������:setAccess_key(String arg); Ŀǰֻ֧��*String*���͵Ĳ�����
         * *displayName* Ϊ������ʾ����ͬ����Ϊ��UI�����Ŀ��ǣ������û��������ɸ��ݲ����б�̬��ʾ��UI���档
         * ������ֵ����ֱ�������������ļ��У�Ҳ�����������ڶ�̬��ֵ��ֱ������ֵ������ֱ��ʹ�ú�˽ӿ���˵��Ϊ���㡣����UI������˵�������ڶ�̬��ֵ��Ϊ����<br/></br>

     ��ʹ��Դ�빤��ʱ����������ļ�ͳһ�����ڹ��̵�*plugins*Ŀ¼�¡���Ҳ����ͳһ�������κ�λ�á���ʱ���ڹ����˽ӿ�ʵ��ʱ����Ҫ��֪�ӿڸ�λ�á�
   
<a name="ʹ��ShurnimStorage�ӿ�"></a>
### ʹ��*ShurnimStorage*�ӿ�

<a name="�ӿڽ���"></a>
#### �ӿڽ���

**ShurnimStorage**�ӿ���*shurinm-storage*���ȫ�ֵ�Ҳ��Ψһ�Ľӿڣ�Ŀǰ������

```
package com.coderli.shurnim.storage;

import java.util.List;
import java.util.Map;

import com.coderli.shurnim.storage.plugin.model.Plugin;
import com.coderli.shurnim.storage.plugin.model.Resource;

/**
* ��̨ģ���ȫ�ֽӿ�<br>
* ͨ���ýӿ�ʹ�ú�̨��ȫ�����ܡ�<br>
* ʹ�÷�ʽ:<br>
* <li>
* 1.��ͨ��{@link #getSupportedPlugins()}������ȡ����֧�ֵ�ƽ̨/����б� <li>
* 2.���б��з��ص�ID�����Ӧ�Ľӿڲ����У����ж�Ӧ��ƽ̨����ز�����<br>
* ��Ҫע����ǣ���ͬƽ̨�Ĳ����Ҫ����ͬ�Ĳ�����ֵ����ֵ����ֱ�������������ļ��С�<br>
* Ҳ�����������ڶ�̬��ֵ��(�Ḳ�������ļ��е�ֵ��)<br>
*
* �����б����ƣ�����UI������Ա��̬�ĸ��ݲ����б����ɿ���д�Ŀؼ�������������ֵ����ǿ�˿���չ�ԡ�
*
* @author OneCoder
* @date 2014��4��22�� ����9:21:58
* @website http://www.coderli.com
*/
public interface ShurnimStorage {

     /**
      * ��ȡ��ǰ֧�ֵĲ���б�<br>
      * û��֧�ֵĲ����ʱ����ܷ���null
      *
      * @return
      * @author OneCoder
      * @date 2014��5��7�� ����8:53:25
      */
     List<Plugin> getSupportedPlugins();

     /**
      * ��ָ���Ĳ���Ķ�Ӧ������ֵ<br>
      * �˴���ֵ�Ḳ�������ļ��е�Ĭ��ֵ
      *
      * @param pluginId
      *            ���ID
      * @param paramsKV
      *            ������ֵ��
      * @author OneCoder
      * @date 2014��5��9�� ����12:41:53
      */
     void setParamValues(String pluginId, Map<String, String> paramsKV);

     /**
      * ��ȡ�����ӦĿ¼�µ���Դ�б�
      *
      * @param pluginId
      *            ���ID
      * @param path
      *            ָ��·��
      * @return
      * @author OneCoder
      * @date 2014��5��11�� ����8:52:00
      */
     List<Resource> getResources(String pluginId, String path);

     /**
      * ͬ����Դ
      *
      * @param fromPluginId
      *            ��ͬ���Ĳ��Id
      * @param toPluginIds
      *            Ŀ����Id
      * @param resource
      *            ��ͬ������Դ
      * @return ͬ�����
      * @author OneCoder
      * @date 2014��5��11�� ����11:41:24
      */
     boolean sycnResource(String fromPluginId, String toPluginId,
                    Resource resource) throws Exception;
}
```    

��ǰ�ӿ�ʵ�ʽ������˻�ȡ��Դ�б�*getResources*��ͬ����Դ*sycnResource*���ܣ�*getSupportedPlugins*��*setParamValues*ʵ��Ϊ�����ӿڣ���UI����ʱ��Ϊ���á�<br/><br/>
ͬ������Ҳ������չ�����ýӿ����Ӹ������ϲ�������ԡ����磬ͬʱɾ�������洢�ϵ��ļ�����Ȼ������Ҫ����ӿڵ����֧�֡�<br/><br/>

���*sycnResource*��Ƴɲ����һ��һ����ʽ���ǿ��ǵ���ȡͬ���Ƿ�ɹ��Ľ��������������뿪��һ��ͬ��������洢�Ĺ��ܣ����������¿������Լ��Ľӿ�ʵ���࣬��ΪĬ��ʵ�ֻ����´���Դ(ÿ��ͬ����ɾ��)�����������Դ���˷ѡ�

�ӿڵ�Ĭ��ʵ������: **DefaultShurnimStorageImpl**

<a name="ʹ������"></a>
#### ʹ������
```      
package com.coderli.shurnim.test.shurnimstorage;

import org.junit.Assert;
import org.junit.BeforeClass;
import org.junit.Test;

import com.coderli.shurnim.storage.DefaultShurnimStorageImpl;
import com.coderli.shurnim.storage.ShurnimStorage;
import com.coderli.shurnim.storage.plugin.model.Resource;
import com.coderli.shurnim.storage.plugin.model.Resource.Type;

/**
* ȫ�ֽӿڲ�����<br>
* ʱ�����ޣ�Ŀǰ��������ӿڲ��ԡ�ϸ���ȵĵ�Ԫ���ԣ��濪�����䡣
*
* @author OneCoder
* @date 2014��5��19�� ����10:50:27
* @website http://www.coderli.com
*/
public class ShurnimStorageTest {

     private static ShurnimStorage shurnim;

     @BeforeClass
     public static void init() {
          shurnim = new DefaultShurnimStorageImpl(
                    "/Users/apple/git/shurnim-storage-for-UPYUN/plugins");
     }

     @Test
     public void testSycnResource() {
          Resource syncResource = new Resource();
          syncResource.setPath("/api");
          syncResource.setName("api.html");
          syncResource.setType(Type.FILE);
          try {
               Assert.assertTrue(shurnim.sycnResource("upyun", "qiniu",
                         syncResource));
          } catch (Exception e) {
               e.printStackTrace();
          }
     }
}
```
<a name="����"></a>
## ����

ʱ��ִ٣����ܼ�ª������������OneCoder(Blog:[http://www.coderli.com](http://www.coderli.com))�ر�ϣ����������Ŀ��������һ���İ��������������ͽ��飬��ӭ�������ҹ�ͨ,��ϵ��ʽ��

* Email: <wushikezuo@gmail.com>
* QQ:57959968
* Blog:[OneCoder](http://www.coderli.com)

��Ŀ��Bug�͸Ľ��㣬����OSChina����issue�ķ�ʽֱ���ύ���ҡ�