---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012303"
---
# <span data-ttu-id="695b1-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="695b1-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="695b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="695b1-102">SYNOPSIS</span></span>
<span data-ttu-id="695b1-103">A címtárból vagy a fájlrendszer gyökeréből származó alkönyvtárak és fájlok listázása.</span><span class="sxs-lookup"><span data-stu-id="695b1-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="695b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="695b1-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="695b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="695b1-105">DESCRIPTION</span></span>
<span data-ttu-id="695b1-106">A **Get-AzDataLakeGen2ChildItem** parancsmag az Azure tárterület-fiókban lévő címtárban vagy filesystemben található alkönyvtárak és fájlok listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="695b1-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="695b1-107">Ez a parancsmag csak akkor működik, ha a tároló fiókhoz engedélyezve van a hierarchikus névtér.</span><span class="sxs-lookup"><span data-stu-id="695b1-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="695b1-108">Ezt a típusú fiókot úgy hozhatja létre, hogy a "New-AzStorageAccount" parancsmagot futtatja a "-EnableHierarchicalNamespace $true" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="695b1-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="695b1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="695b1-109">EXAMPLES</span></span>

### <span data-ttu-id="695b1-110">Példa 1: a közvetlen alelemek listázása egy fájlrendszerből</span><span class="sxs-lookup"><span data-stu-id="695b1-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="695b1-111">Ez a parancs felsorolja a közvetlen alelemeket egy fájlrendszerből</span><span class="sxs-lookup"><span data-stu-id="695b1-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="695b1-112">2. példa: a lista rekurzív módon lett egy címtárból, és a beolvasás tulajdonságai/ACL</span><span class="sxs-lookup"><span data-stu-id="695b1-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="695b1-113">Ez a parancs felsorolja a közvetlen alelemeket egy fájlrendszerből</span><span class="sxs-lookup"><span data-stu-id="695b1-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="695b1-114">3. példa: listaelemek rekurzív létrehozása több kötegben</span><span class="sxs-lookup"><span data-stu-id="695b1-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="695b1-115">Ebben a példában a *MaxCount* és a *ContinuationToken* paraméterrel több kötegből álló fájlrendszerből listázhatja az elemeket.</span><span class="sxs-lookup"><span data-stu-id="695b1-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="695b1-116">Az első négy parancs az értékeket a példában használt változókhoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="695b1-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="695b1-117">Az ötödik parancs olyan **do-while** utasítást ad meg, amely a **Get-AzDataLakeGen2ChildItem** parancsmagot használja az elemek listázásához.</span><span class="sxs-lookup"><span data-stu-id="695b1-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="695b1-118">Az utasítás tartalmazza a $Token változóban tárolt folytatólagos tokent.</span><span class="sxs-lookup"><span data-stu-id="695b1-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="695b1-119">$Token az érték ismétléssel változik.</span><span class="sxs-lookup"><span data-stu-id="695b1-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="695b1-120">A végleges parancs a **echo** parancs segítségével jeleníti meg a végösszeget.</span><span class="sxs-lookup"><span data-stu-id="695b1-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="695b1-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="695b1-121">PARAMETERS</span></span>

### <span data-ttu-id="695b1-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="695b1-122">-AsJob</span></span>
<span data-ttu-id="695b1-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="695b1-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b1-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="695b1-124">-Context</span></span>
<span data-ttu-id="695b1-125">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="695b1-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="695b1-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="695b1-126">-ContinuationToken</span></span>
<span data-ttu-id="695b1-127">Folytatólagos jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="695b1-127">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695b1-128">-DefaultProfile</span></span>
<span data-ttu-id="695b1-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="695b1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="695b1-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="695b1-130">-FetchProperty</span></span>
<span data-ttu-id="695b1-131">A datalake és az ACL elem beolvasása</span><span class="sxs-lookup"><span data-stu-id="695b1-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b1-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="695b1-132">-FileSystem</span></span>
<span data-ttu-id="695b1-133">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="695b1-133">FileSystem name</span></span>

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

### <span data-ttu-id="695b1-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="695b1-134">-MaxCount</span></span>
<span data-ttu-id="695b1-135">Az eredményül kapott Blobok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="695b1-135">The max count of the blobs that can return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b1-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="695b1-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="695b1-137">Ha a speicify ezt a paramétert adja meg, a program az egyes listaelemek tulajdonos és csoport mezőiből visszaadott felhasználói identitási értékeket az Azure Active Directory-objektum-azonosítók alapján átalakítja a felhasználók egyszerű neveire.</span><span class="sxs-lookup"><span data-stu-id="695b1-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="695b1-138">Ha a paraméter nem speicify, az értékek az Azure Active Directory Object ID-ként lesznek visszaadva.</span><span class="sxs-lookup"><span data-stu-id="695b1-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="695b1-139">Figyelje meg, hogy a csoport-és alkalmazásobjektum-azonosítók nincsenek lefordítva, mert nincsenek egyedi felhasználóbarát nevei.</span><span class="sxs-lookup"><span data-stu-id="695b1-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b1-140">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="695b1-140">-Path</span></span>
<span data-ttu-id="695b1-141">A megadott filesystem elérési útja, amelyet le kell olvasni.</span><span class="sxs-lookup"><span data-stu-id="695b1-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="695b1-142">A "directory1/directory2/" formátumban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="695b1-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="695b1-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="695b1-143">-Recurse</span></span>
<span data-ttu-id="695b1-144">Azt jelzi, hogy a program rekurzívan kapja-e a gyermek elemét.</span><span class="sxs-lookup"><span data-stu-id="695b1-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="695b1-145">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="695b1-145">The default is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695b1-146">CommonParameters</span></span>
<span data-ttu-id="695b1-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="695b1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695b1-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="695b1-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695b1-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="695b1-149">INPUTS</span></span>

### <span data-ttu-id="695b1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="695b1-150">System.String</span></span>

### <span data-ttu-id="695b1-151">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="695b1-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="695b1-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="695b1-152">OUTPUTS</span></span>

### <span data-ttu-id="695b1-153">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="695b1-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="695b1-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="695b1-154">NOTES</span></span>

## <span data-ttu-id="695b1-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="695b1-155">RELATED LINKS</span></span>
