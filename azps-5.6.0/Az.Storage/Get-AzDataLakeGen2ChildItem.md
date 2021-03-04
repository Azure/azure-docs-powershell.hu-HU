---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 3505d9b07e1d56936a002b45bfeee7929823f4be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935481"
---
# <span data-ttu-id="59076-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="59076-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="59076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59076-102">SYNOPSIS</span></span>
<span data-ttu-id="59076-103">A címtárból vagy a fájlrendszer gyökérkönyvtáraiból származó alkönyvtárak és fájlok listája.</span><span class="sxs-lookup"><span data-stu-id="59076-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="59076-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59076-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59076-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59076-105">DESCRIPTION</span></span>
<span data-ttu-id="59076-106">A **Get-AzDataLakeGen2DataItem** parancsmag egy Azure-tárfiók címtárában vagy fájlrendszerében található alkönyvtárak és fájlok listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="59076-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="59076-107">Ez a parancsmag csak akkor működik, ha engedélyezve van a Hierarchikus névtér a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="59076-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="59076-108">Az ilyen típusú fiók az "-EnableHierarchicalNamespace $true" parancsmag futtatásával $true.</span><span class="sxs-lookup"><span data-stu-id="59076-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="59076-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59076-109">EXAMPLES</span></span>

### <span data-ttu-id="59076-110">1. példa: A fájlrendszerből származó közvetlen alelemek felsorolása</span><span class="sxs-lookup"><span data-stu-id="59076-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="59076-111">Ez a parancs felsorolja a filesystemből származó közvetlen alelemeket</span><span class="sxs-lookup"><span data-stu-id="59076-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="59076-112">2. példa: Címtárból rekurzív lista, és tulajdonságok/ACL lehívása</span><span class="sxs-lookup"><span data-stu-id="59076-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="59076-113">Ez a parancs felsorolja a filesystemből származó közvetlen alelemeket</span><span class="sxs-lookup"><span data-stu-id="59076-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="59076-114">3. példa: Több kötegben egy fájlrendszerből rekurzív listaelemek</span><span class="sxs-lookup"><span data-stu-id="59076-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
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

<span data-ttu-id="59076-115">Ebben a példában a *MaxCount* és *a ContinuationToken* paramétert használva több kötegben listába soroljuk a fájlrendszerből rekurzív elemeket.</span><span class="sxs-lookup"><span data-stu-id="59076-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="59076-116">Az első négy parancs értékeket rendel a példában használt változókhoz.</span><span class="sxs-lookup"><span data-stu-id="59076-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="59076-117">Az ötödik parancs egy **Olyan Do-While utasítást** ad meg, amely a **Get-AzDataLakeGen2DataItem** parancsmagot használja az elemek listájához.</span><span class="sxs-lookup"><span data-stu-id="59076-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="59076-118">Az utasítás tartalmazza a $Token változóban tárolt $Token tokent.</span><span class="sxs-lookup"><span data-stu-id="59076-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="59076-119">$Token a hurok futásakor megváltozik az érték.</span><span class="sxs-lookup"><span data-stu-id="59076-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="59076-120">Az utolsó parancs a **Visszhang paranccsal** jeleníti meg az összeget.</span><span class="sxs-lookup"><span data-stu-id="59076-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="59076-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59076-121">PARAMETERS</span></span>

### <span data-ttu-id="59076-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59076-122">-AsJob</span></span>
<span data-ttu-id="59076-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="59076-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59076-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="59076-124">-Context</span></span>
<span data-ttu-id="59076-125">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="59076-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="59076-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="59076-126">-ContinuationToken</span></span>
<span data-ttu-id="59076-127">Folytatási jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="59076-127">Continuation Token.</span></span>

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

### <span data-ttu-id="59076-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59076-128">-DefaultProfile</span></span>
<span data-ttu-id="59076-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59076-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59076-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="59076-130">-FetchProperty</span></span>
<span data-ttu-id="59076-131">Lekéri az adatkapcsolatú elemek tulajdonságait és az ACL-et.</span><span class="sxs-lookup"><span data-stu-id="59076-131">Fetch the datalake item properties and ACL.</span></span>

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

### <span data-ttu-id="59076-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="59076-132">-FileSystem</span></span>
<span data-ttu-id="59076-133">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="59076-133">FileSystem name</span></span>

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

### <span data-ttu-id="59076-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="59076-134">-MaxCount</span></span>
<span data-ttu-id="59076-135">A visszaadott blobok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="59076-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="59076-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="59076-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="59076-137">Ha ezt a paramétert speicify, az egyes listabejegyzések tulajdonosi és csoportmezőiben visszaadott felhasználói identitásértékek Azure Active Directory-objektum-azonosítókból egyszerű felhasználónevekké alakulnak át.</span><span class="sxs-lookup"><span data-stu-id="59076-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="59076-138">Ha nem speicify ez a paraméter, az értékeket a rendszer Azure Active Directory-objektum-adatokat ad vissza.</span><span class="sxs-lookup"><span data-stu-id="59076-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="59076-139">Felhívjuk a figyelmét arra, hogy a csoport- és alkalmazásobjektum-azonosítókat nem fordítja a program, mert nem rendelkezik egyedi felhasználóbarát névvel.</span><span class="sxs-lookup"><span data-stu-id="59076-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

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

### <span data-ttu-id="59076-140">-Path</span><span class="sxs-lookup"><span data-stu-id="59076-140">-Path</span></span>
<span data-ttu-id="59076-141">A megadott fájlrendszerben lekérni kívánt elérési út.</span><span class="sxs-lookup"><span data-stu-id="59076-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="59076-142">Címtárnak kell lennie, "directory1/directory2/" formátumban.</span><span class="sxs-lookup"><span data-stu-id="59076-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="59076-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="59076-143">-Recurse</span></span>
<span data-ttu-id="59076-144">Azt jelzi, hogy rekurzívan be fogja-e szerezni a gyermekelemet.</span><span class="sxs-lookup"><span data-stu-id="59076-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="59076-145">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="59076-145">The default is false.</span></span>

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

### <span data-ttu-id="59076-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59076-146">CommonParameters</span></span>
<span data-ttu-id="59076-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59076-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59076-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59076-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59076-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59076-149">INPUTS</span></span>

### <span data-ttu-id="59076-150">System.String</span><span class="sxs-lookup"><span data-stu-id="59076-150">System.String</span></span>

### <span data-ttu-id="59076-151">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59076-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59076-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59076-152">OUTPUTS</span></span>

### <span data-ttu-id="59076-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="59076-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="59076-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59076-154">NOTES</span></span>

## <span data-ttu-id="59076-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59076-155">RELATED LINKS</span></span>
