---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374134"
---
# <span data-ttu-id="d3c2e-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d3c2e-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="d3c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c2e-103">Egy fájlrendszerben található fájl vagy címtár részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="d3c2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3c2e-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3c2e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="d3c2e-106">A **Get-AzDataLakeGen2Item** parancsmag egy Azure-tárfiók fájlrendszerében található fájl vagy címtár adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="d3c2e-107">Ez a parancsmag csak akkor működik, ha engedélyezve van a Hierarchikus névtér a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="d3c2e-108">Az ilyen típusú fiók az "-EnableHierarchicalNamespace $true" parancsmag futtatásával $true.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="d3c2e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3c2e-109">EXAMPLES</span></span>

### <span data-ttu-id="d3c2e-110">1. példa: Könyvtár lekérte egy fájlrendszerből, és a részletek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d3c2e-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
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

<span data-ttu-id="d3c2e-111">Ez a parancs egy könyvtárat kap egy fájlrendszerből, és megmutatja a részleteket.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="d3c2e-112">2. példa: Fájl lekérte egy fájlrendszerből</span><span class="sxs-lookup"><span data-stu-id="d3c2e-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="d3c2e-113">Ez a parancs a fájl részleteit egy fájlrendszerből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="d3c2e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3c2e-114">PARAMETERS</span></span>

### <span data-ttu-id="d3c2e-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d3c2e-115">-Context</span></span>
<span data-ttu-id="d3c2e-116">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="d3c2e-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d3c2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c2e-117">-DefaultProfile</span></span>
<span data-ttu-id="d3c2e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3c2e-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="d3c2e-119">-FileSystem</span></span>
<span data-ttu-id="d3c2e-120">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="d3c2e-120">FileSystem name</span></span>

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

### <span data-ttu-id="d3c2e-121">-Path</span><span class="sxs-lookup"><span data-stu-id="d3c2e-121">-Path</span></span>
<span data-ttu-id="d3c2e-122">A megadott fájlrendszerben lekérni kívánt elérési út.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="d3c2e-123">Fájl vagy címtár lehet "directory/file.txt" vagy "directory1/directory2/".</span><span class="sxs-lookup"><span data-stu-id="d3c2e-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="d3c2e-124">Ez a paraméter nem adható meg a Filesystem gyökérkönyvtárának be szereznie.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="d3c2e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c2e-125">CommonParameters</span></span>
<span data-ttu-id="d3c2e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c2e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c2e-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c2e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c2e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3c2e-128">INPUTS</span></span>

### <span data-ttu-id="d3c2e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d3c2e-129">System.String</span></span>

### <span data-ttu-id="d3c2e-130">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3c2e-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d3c2e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3c2e-131">OUTPUTS</span></span>

### <span data-ttu-id="d3c2e-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d3c2e-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="d3c2e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3c2e-133">NOTES</span></span>

## <span data-ttu-id="d3c2e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3c2e-134">RELATED LINKS</span></span>
