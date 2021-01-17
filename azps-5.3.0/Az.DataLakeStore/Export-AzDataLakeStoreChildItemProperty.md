---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465850"
---
# <span data-ttu-id="f3811-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="f3811-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="f3811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3811-102">SYNOPSIS</span></span>
<span data-ttu-id="f3811-103">Exportálja a teljes fa tulajdonságait (lemezhasználat és Acl) a megadott elérési útból a kimeneti útvonalra.</span><span class="sxs-lookup"><span data-stu-id="f3811-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="f3811-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3811-104">SYNTAX</span></span>

### <span data-ttu-id="f3811-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="f3811-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3811-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="f3811-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3811-107">GetAclDcsonk</span><span class="sxs-lookup"><span data-stu-id="f3811-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3811-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3811-108">DESCRIPTION</span></span>
<span data-ttu-id="f3811-109">Az **Export-AzDataLakeStoreDataItemProperty** a megadott címtár ADLS-tárhelyhasználatának, illetve/vagy ACL-használatának, valamint alkönyvtáraknak és fájloknak a jelentésére használható.</span><span class="sxs-lookup"><span data-stu-id="f3811-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="f3811-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3811-110">EXAMPLES</span></span>

### <span data-ttu-id="f3811-111">1. példa: A lemezhasználat és az ACL-használat lekérte az összes alkönyvtárra és fájlra</span><span class="sxs-lookup"><span data-stu-id="f3811-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="f3811-112">A /a alkönyvtárak és fájlok lemezhasználatának és ACL-használatának lekérte.</span><span class="sxs-lookup"><span data-stu-id="f3811-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="f3811-113">IncludeFile ensures the usage is reported for files</span><span class="sxs-lookup"><span data-stu-id="f3811-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="f3811-114">2. példa: Az összes alkönyvtár és fájl ACL-használatának lekérte a rejtett konzisztens ACL-t</span><span class="sxs-lookup"><span data-stu-id="f3811-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="f3811-115">Az ACL használata az összes alkönyvtárhoz és fájlhoz a /a alatt.</span><span class="sxs-lookup"><span data-stu-id="f3811-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="f3811-116">Az IncludeFile gondoskodik arról, hogy a fájlok használata is jelentve legyen.</span><span class="sxs-lookup"><span data-stu-id="f3811-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="f3811-117">HideconsistentAcl ebben az esetben az Acl of /a-t fogja mutatni, nem pedig a gyermekekét, mivel az összes gyermeknek ugyanaz acl-jük, mint a /a.</span><span class="sxs-lookup"><span data-stu-id="f3811-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="f3811-118">Ez a jelölő kihagyja a részfában acl kimenetet, ha az összes acls megegyezik a gyökérvel.</span><span class="sxs-lookup"><span data-stu-id="f3811-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="f3811-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3811-119">PARAMETERS</span></span>

### <span data-ttu-id="f3811-120">-Account</span><span class="sxs-lookup"><span data-stu-id="f3811-120">-Account</span></span>
<span data-ttu-id="f3811-121">The Data Lake Store account to execute the filesystem operation in</span><span class="sxs-lookup"><span data-stu-id="f3811-121">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-122">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="f3811-122">-Concurrency</span></span>
<span data-ttu-id="f3811-123">A párhuzamosan feldolgozott fájlok/könyvtárak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="f3811-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="f3811-124">Az alapértelmezett érték a rendszer specifikációja alapján számítható legjobb munkamennyiségként.</span><span class="sxs-lookup"><span data-stu-id="f3811-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3811-125">-DefaultProfile</span></span>
<span data-ttu-id="f3811-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3811-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="f3811-127">-GetAcl</span></span>
<span data-ttu-id="f3811-128">A gyökér elérési úttól kezdve beolvassa az acl-et</span><span class="sxs-lookup"><span data-stu-id="f3811-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="f3811-129">-GetDiskUsage</span></span>
<span data-ttu-id="f3811-130">A gyökér elérési úttól kezdve beolvassa a lemezhasználatot</span><span class="sxs-lookup"><span data-stu-id="f3811-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="f3811-131">-HideConsistentAcl</span></span>
<span data-ttu-id="f3811-132">Ne mutassa a címtár-résztűrt, ha az ACL-ek a teljes részében azonosak.</span><span class="sxs-lookup"><span data-stu-id="f3811-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="f3811-133">Így könnyebben láthatja, hogy milyen útvonalakon térnek el az ACLs-ek. Ha például a /a/b csoportban lévő összes fájl és mappa megegyezik, ne legyen látható a subtreeunder /a/b, és csak az "Igaz" kimenet legyen beállítva a Konzisztens ACL oszlopban, ha az IncludeFiles nincs beállítva, mert az egységes Acl nem határozható meg a fájlokcl-ének beolvasása nélkül.</span><span class="sxs-lookup"><span data-stu-id="f3811-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="f3811-134">-IncludeFile</span></span>
<span data-ttu-id="f3811-135">A statok megjelenítése fájlszinten (alapértelmezés szerint csak a címtárszintű adatokat mutatja)</span><span class="sxs-lookup"><span data-stu-id="f3811-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="f3811-136">-MaximumDepth</span></span>
<span data-ttu-id="f3811-137">A legfelső szintű címtártól a lemezhasználat vagy azcl megjelenítésének maximális mélysége</span><span class="sxs-lookup"><span data-stu-id="f3811-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f3811-138">-OutputPath</span></span>
<span data-ttu-id="f3811-139">A kimeneti fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f3811-139">Path to output file.</span></span> <span data-ttu-id="f3811-140">Lehet helyi elérési út vagy Adl elérési út.</span><span class="sxs-lookup"><span data-stu-id="f3811-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="f3811-141">Alapértelmezés szerint helyi.</span><span class="sxs-lookup"><span data-stu-id="f3811-141">By default it is local.</span></span> <span data-ttu-id="f3811-142">Ha a SaveToAdl érték meg van adva, akkor az egy ADL-elérési út ugyanabban a fiókban</span><span class="sxs-lookup"><span data-stu-id="f3811-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3811-143">-PassThru</span></span>
<span data-ttu-id="f3811-144">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="f3811-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-145">-Path</span><span class="sxs-lookup"><span data-stu-id="f3811-145">-Path</span></span>
<span data-ttu-id="f3811-146">A megadott Data Lake-fiókban lekérni szükséges elérési út.</span><span class="sxs-lookup"><span data-stu-id="f3811-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="f3811-147">Fájl vagy mappa lehet "/folder/file.txt" formátumban, ahol a DNS utáni első "/" a fájlrendszer gyökerét jelzi.</span><span class="sxs-lookup"><span data-stu-id="f3811-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="f3811-148">-SaveToAdl</span></span>
<span data-ttu-id="f3811-149">Ha a rendszer ezt követően menti a kukát az ADL-be.</span><span class="sxs-lookup"><span data-stu-id="f3811-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="f3811-150">Ebben az esetben a DumpFile egy ADL-útvonal</span><span class="sxs-lookup"><span data-stu-id="f3811-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3811-151">-Confirm</span></span>
<span data-ttu-id="f3811-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3811-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3811-153">-WhatIf</span></span>
<span data-ttu-id="f3811-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3811-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3811-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3811-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3811-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3811-156">CommonParameters</span></span>
<span data-ttu-id="f3811-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3811-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3811-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3811-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3811-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3811-159">INPUTS</span></span>

### <span data-ttu-id="f3811-160">System.String</span><span class="sxs-lookup"><span data-stu-id="f3811-160">System.String</span></span>

### <span data-ttu-id="f3811-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f3811-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f3811-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3811-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f3811-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f3811-163">System.Int32</span></span>

## <span data-ttu-id="f3811-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3811-164">OUTPUTS</span></span>

### <span data-ttu-id="f3811-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3811-165">System.Boolean</span></span>

## <span data-ttu-id="f3811-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3811-166">NOTES</span></span>

## <span data-ttu-id="f3811-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3811-167">RELATED LINKS</span></span>
