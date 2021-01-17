---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371418"
---
# <span data-ttu-id="5b7a1-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="5b7a1-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="5b7a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7a1-103">Exportálja a teljes fa tulajdonságait (lemezhasználat és Acl) a megadott elérési útból egy kimeneti útvonalra.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="5b7a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b7a1-104">SYNTAX</span></span>

### <span data-ttu-id="5b7a1-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="5b7a1-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b7a1-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="5b7a1-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7a1-107">GetAclDcsonk</span><span class="sxs-lookup"><span data-stu-id="5b7a1-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b7a1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b7a1-108">DESCRIPTION</span></span>
<span data-ttu-id="5b7a1-109">Az **Export-AzDataLakeStoreDataItemProperty** az adott címtár ADLS-tárhelyhasználatának vagy/vagy/vagy ACL-használatának, valamint alkönyvtáraknak és fájloknak a jelentésére használható.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="5b7a1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b7a1-110">EXAMPLES</span></span>

### <span data-ttu-id="5b7a1-111">1. példa: A lemezhasználat és az ACL-használat lekérte az összes alkönyvtárra és fájlra</span><span class="sxs-lookup"><span data-stu-id="5b7a1-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="5b7a1-112">Szerezze be a lemezhasználatot és az ACL-használatot az /a alatti összes alkönyvtárhoz és fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="5b7a1-113">IncludeFile ensures the usage is reported for files</span><span class="sxs-lookup"><span data-stu-id="5b7a1-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="5b7a1-114">2. példa: Az összes alkönyvtár és fájl ACL-használatának lekérte a rejtett konzisztens ACL-t</span><span class="sxs-lookup"><span data-stu-id="5b7a1-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="5b7a1-115">Az ACL használata az összes alkönyvtárhoz és fájlhoz a /a alatt.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="5b7a1-116">Az IncludeFile gondoskodik arról, hogy a fájlok használata is jelentve legyen.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="5b7a1-117">HideconsistentAcl ebben az esetben az Acl of /a-t fogja mutatni, nem pedig a gyermekekét, mivel az összes gyermeknek ugyanaz acl-jük, mint a /a.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="5b7a1-118">Ez a jelölő kihagyja a részfában acl kimenetet, ha az összes acls megegyezik a gyökérvel.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="5b7a1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b7a1-119">PARAMETERS</span></span>

### <span data-ttu-id="5b7a1-120">-Account</span><span class="sxs-lookup"><span data-stu-id="5b7a1-120">-Account</span></span>
<span data-ttu-id="5b7a1-121">The Data Lake Store account to execute the filesystem operation in</span><span class="sxs-lookup"><span data-stu-id="5b7a1-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="5b7a1-122">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="5b7a1-122">-Concurrency</span></span>
<span data-ttu-id="5b7a1-123">A párhuzamosan feldolgozott fájlok/könyvtárak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="5b7a1-124">Az alapértelmezett érték a rendszer specifikációja alapján számítható legjobb munkamennyiségként.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="5b7a1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7a1-125">-DefaultProfile</span></span>
<span data-ttu-id="5b7a1-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b7a1-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="5b7a1-127">-GetAcl</span></span>
<span data-ttu-id="5b7a1-128">A gyökér elérési úttól kezdve beolvassa az acl-et</span><span class="sxs-lookup"><span data-stu-id="5b7a1-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="5b7a1-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="5b7a1-129">-GetDiskUsage</span></span>
<span data-ttu-id="5b7a1-130">A gyökér elérési úttól kezdve beolvassa a lemezhasználatot</span><span class="sxs-lookup"><span data-stu-id="5b7a1-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="5b7a1-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="5b7a1-131">-HideConsistentAcl</span></span>
<span data-ttu-id="5b7a1-132">Ne mutassa a címtár-résztűrt, ha az ACL-ek a teljes részében azonosak.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="5b7a1-133">Így könnyebben láthatja, hogy milyen elérési utakon térnek el az ACL-ek. Ha például a /a/b csoportban lévő összes fájl és mappa megegyezik, ne legyen látható a subtreeunder /a/b, és csak az "Igaz" kimenet legyen beállítva a Konzisztens ACL oszlopban, ha az IncludeFiles nincs beállítva, mert a konzisztens Acl nem határozható meg a fájlokcl-ének beolvasása nélkül.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="5b7a1-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="5b7a1-134">-IncludeFile</span></span>
<span data-ttu-id="5b7a1-135">A statok megjelenítése fájlszinten (alapértelmezés szerint csak a címtárszintű adatok megjelenítése)</span><span class="sxs-lookup"><span data-stu-id="5b7a1-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="5b7a1-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="5b7a1-136">-MaximumDepth</span></span>
<span data-ttu-id="5b7a1-137">A legfelső szintű címtártól a lemezhasználat vagy az acl megjelenítésének maximális mélysége</span><span class="sxs-lookup"><span data-stu-id="5b7a1-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="5b7a1-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="5b7a1-138">-OutputPath</span></span>
<span data-ttu-id="5b7a1-139">A kimeneti fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-139">Path to output file.</span></span> <span data-ttu-id="5b7a1-140">Lehet helyi elérési út vagy Adl elérési út.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="5b7a1-141">Alapértelmezés szerint helyi.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-141">By default it is local.</span></span> <span data-ttu-id="5b7a1-142">Ha a SaveToAdl érték meg van adva, akkor az egy ADL-elérési út ugyanabban a fiókban</span><span class="sxs-lookup"><span data-stu-id="5b7a1-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="5b7a1-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b7a1-143">-PassThru</span></span>
<span data-ttu-id="5b7a1-144">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="5b7a1-145">-Path</span><span class="sxs-lookup"><span data-stu-id="5b7a1-145">-Path</span></span>
<span data-ttu-id="5b7a1-146">A megadott Data Lake-fiókban lekérni szükséges elérési út.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="5b7a1-147">Fájl vagy mappa lehet "/folder/file.txt" formátumban, ahol a DNS utáni első "/" a fájlrendszer gyökerét jelzi.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="5b7a1-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="5b7a1-148">-SaveToAdl</span></span>
<span data-ttu-id="5b7a1-149">Ha a rendszer ezt követően menti a kukát az ADL-be.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="5b7a1-150">Ebben az esetben a DumpFile egy ADL-elérési út</span><span class="sxs-lookup"><span data-stu-id="5b7a1-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="5b7a1-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b7a1-151">-Confirm</span></span>
<span data-ttu-id="5b7a1-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b7a1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b7a1-153">-WhatIf</span></span>
<span data-ttu-id="5b7a1-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b7a1-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b7a1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7a1-156">CommonParameters</span></span>
<span data-ttu-id="5b7a1-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b7a1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7a1-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b7a1-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7a1-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b7a1-159">INPUTS</span></span>

### <span data-ttu-id="5b7a1-160">System.String</span><span class="sxs-lookup"><span data-stu-id="5b7a1-160">System.String</span></span>

### <span data-ttu-id="5b7a1-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5b7a1-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5b7a1-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5b7a1-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5b7a1-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5b7a1-163">System.Int32</span></span>

## <span data-ttu-id="5b7a1-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7a1-164">OUTPUTS</span></span>

### <span data-ttu-id="5b7a1-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b7a1-165">System.Boolean</span></span>

## <span data-ttu-id="5b7a1-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b7a1-166">NOTES</span></span>

## <span data-ttu-id="5b7a1-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b7a1-167">RELATED LINKS</span></span>
