---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: ffbfad973e881c3ae88e961517d097d7c8d6cedd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012305"
---
# <span data-ttu-id="32aa8-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="32aa8-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="32aa8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="32aa8-103">Egy fájlrendszerben lévő fájl vagy könyvtár részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="32aa8-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="32aa8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32aa8-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32aa8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="32aa8-106">A **Get-AzDataLakeGen2Item** parancsmag az Azure Storage-fiókjában található fájl vagy könyvtár adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="32aa8-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="32aa8-107">Ez a parancsmag csak akkor működik, ha a tároló fiókhoz engedélyezve van a hierarchikus névtér.</span><span class="sxs-lookup"><span data-stu-id="32aa8-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="32aa8-108">Ezt a típusú fiókot úgy hozhatja létre, hogy a "New-AzStorageAccount" parancsmagot futtatja a "-EnableHierarchicalNamespace $true" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="32aa8-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="32aa8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="32aa8-109">EXAMPLES</span></span>

### <span data-ttu-id="32aa8-110">Példa 1: címtár létrehozása egy fájlrendszerből, és a Részletek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="32aa8-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="32aa8-111">Ez a parancs egy fájlrendszerből kap könyvtárat, és megjeleníti a részleteket.</span><span class="sxs-lookup"><span data-stu-id="32aa8-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="32aa8-112">2. példa: fájl beszerzése fájlrendszerről</span><span class="sxs-lookup"><span data-stu-id="32aa8-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="32aa8-113">Ez a parancs a fájlrendszerből származó fájlok részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="32aa8-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="32aa8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32aa8-114">PARAMETERS</span></span>

### <span data-ttu-id="32aa8-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="32aa8-115">-Context</span></span>
<span data-ttu-id="32aa8-116">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="32aa8-116">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32aa8-117">-DefaultProfile</span></span>
<span data-ttu-id="32aa8-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32aa8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32aa8-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="32aa8-119">-FileSystem</span></span>
<span data-ttu-id="32aa8-120">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="32aa8-120">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa8-121">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="32aa8-121">-Path</span></span>
<span data-ttu-id="32aa8-122">A megadott filesystem elérési útja, amelyet le kell olvasni.</span><span class="sxs-lookup"><span data-stu-id="32aa8-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="32aa8-123">A "címtár/file.txt" vagy a "directory1/directory2/" formátumban lehet fájl vagy könyvtár.</span><span class="sxs-lookup"><span data-stu-id="32aa8-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="32aa8-124">Nem adja meg ezt a paramétert a FileSystem gyökérkönyvtárának beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="32aa8-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32aa8-125">CommonParameters</span></span>
<span data-ttu-id="32aa8-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32aa8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32aa8-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32aa8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32aa8-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32aa8-128">INPUTS</span></span>

### <span data-ttu-id="32aa8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32aa8-129">System.String</span></span>

### <span data-ttu-id="32aa8-130">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="32aa8-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="32aa8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32aa8-131">OUTPUTS</span></span>

### <span data-ttu-id="32aa8-132">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="32aa8-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="32aa8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32aa8-133">NOTES</span></span>

## <span data-ttu-id="32aa8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32aa8-134">RELATED LINKS</span></span>
