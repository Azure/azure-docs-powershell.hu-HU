---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: f7c347be55b2d0cde83013454e8396b9eb8f20f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836330"
---
# <span data-ttu-id="4d984-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="4d984-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="4d984-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d984-102">SYNOPSIS</span></span>
<span data-ttu-id="4d984-103">A tulajdonságok (lemezhasználat és ACL) exportálása a teljes fához a megadott elérési úttal egy kimeneti elérési útra</span><span class="sxs-lookup"><span data-stu-id="4d984-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a ouput path</span></span>

## <span data-ttu-id="4d984-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d984-104">SYNTAX</span></span>

### <span data-ttu-id="4d984-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="4d984-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d984-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="4d984-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d984-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="4d984-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d984-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d984-108">DESCRIPTION</span></span>
<span data-ttu-id="4d984-109">Az **AzDataLakeStoreChildItemProperty** az adott könyvtár ADLS és/vagy ACL-használati módjának jelentésére szolgál, valamint az alkönyvtárakra és a fájlokra.</span><span class="sxs-lookup"><span data-stu-id="4d984-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="4d984-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4d984-110">EXAMPLES</span></span>

### <span data-ttu-id="4d984-111">Példa 1: a lemezhasználat és az ACL használatának beszerzése az összes alkönyvtár és fájl esetében</span><span class="sxs-lookup"><span data-stu-id="4d984-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="4d984-112">A lemezhasználat és az ACL használatának beszerzése az összes alkönyvtárra és-fájlra a/a. csoportban</span><span class="sxs-lookup"><span data-stu-id="4d984-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="4d984-113">A IncludeFile biztosítja, hogy a használat a fájlok számára is elérhető legyen</span><span class="sxs-lookup"><span data-stu-id="4d984-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="4d984-114">2. példa: az összes alkönyvtár és fájl ACL-használati felületének beszerzése a konzisztens ACL-fájlokkal</span><span class="sxs-lookup"><span data-stu-id="4d984-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="4d984-115">Az ACL-használat beszerzése az összes alkönyvtárhoz és fájlhoz a/a. csoportban</span><span class="sxs-lookup"><span data-stu-id="4d984-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="4d984-116">A IncludeFile biztosítja, hogy a használat a fájlok számára is jelenteni legyen.</span><span class="sxs-lookup"><span data-stu-id="4d984-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="4d984-117">Ebben az esetben a HideconsistentAcl az/a-as ACL-t jeleníti meg, nem pedig a gyerekeket, mivel az összes gyermeknek ugyanaz a hozzáférése, mint az/a.</span><span class="sxs-lookup"><span data-stu-id="4d984-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="4d984-118">Ez a jelző kihagyja a részfa ACL kimeneti, ha az összes hozzáférés-vezérlési lista megegyezik a legfelső szintű beállítással.</span><span class="sxs-lookup"><span data-stu-id="4d984-118">This flag skips the acl ouput of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="4d984-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d984-119">PARAMETERS</span></span>

### <span data-ttu-id="4d984-120">-Fiók</span><span class="sxs-lookup"><span data-stu-id="4d984-120">-Account</span></span>
<span data-ttu-id="4d984-121">Az adattó áruházbeli fiókja a FileSystem művelet végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="4d984-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="4d984-122">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="4d984-122">-Concurrency</span></span>
<span data-ttu-id="4d984-123">A párhuzamosan feldolgozott fájlok/könyvtárak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="4d984-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="4d984-124">Az alapértelmezett beállítás a rendszerspecifikáción alapuló legjobb munkamennyiségként fog kiszámításra.</span><span class="sxs-lookup"><span data-stu-id="4d984-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="4d984-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d984-125">-DefaultProfile</span></span>
<span data-ttu-id="4d984-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d984-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d984-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="4d984-127">-GetAcl</span></span>
<span data-ttu-id="4d984-128">Az ACL kikeresése a gyökér elérési útjától kezdve</span><span class="sxs-lookup"><span data-stu-id="4d984-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="4d984-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="4d984-129">-GetDiskUsage</span></span>
<span data-ttu-id="4d984-130">A lemezhasználat kikeresése a gyökér elérési útjától kezdve</span><span class="sxs-lookup"><span data-stu-id="4d984-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="4d984-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="4d984-131">-HideConsistentAcl</span></span>
<span data-ttu-id="4d984-132">Ne jelenjen meg a címtár-részfa, ha az ACL-elemek ugyanazok a teljes részfa alatt.</span><span class="sxs-lookup"><span data-stu-id="4d984-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="4d984-133">Ez megkönnyíti csak azokat az elérési utakat látni, amelyek a hozzáférés-vezérlési listáktól függnek. Ha például a/a/b csoport minden fájlja és mappája megegyezik, ne jelenítse meg a subtreeunder/a/b, és a konzisztens ACL-columnCannot csak a "true" értéket tartalmazó kimeneti/a/b adja meg, ha a IncludeFiles nincs beállítva, mert a konzisztens ACL nem határozható meg a fájlok hozzáférési listáinak beolvasása nélkül.</span><span class="sxs-lookup"><span data-stu-id="4d984-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="4d984-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="4d984-134">-IncludeFile</span></span>
<span data-ttu-id="4d984-135">Statisztika megjelenítése a fájl szinten (alapértelmezés szerint csak a címtár szintű adatok jelenjenek meg)</span><span class="sxs-lookup"><span data-stu-id="4d984-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="4d984-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="4d984-136">-MaximumDepth</span></span>
<span data-ttu-id="4d984-137">Maximális színmélység a gyökérkönyvtárból, amíg a lemezhasználat vagy a hozzáférés-vezérlés megjelenik</span><span class="sxs-lookup"><span data-stu-id="4d984-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="4d984-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="4d984-138">-OutputPath</span></span>
<span data-ttu-id="4d984-139">A kimeneti fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="4d984-139">Path to output file.</span></span> <span data-ttu-id="4d984-140">Lehet helyi elérési út vagy ADL elérési útja.</span><span class="sxs-lookup"><span data-stu-id="4d984-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="4d984-141">Alapértelmezés szerint helyi.</span><span class="sxs-lookup"><span data-stu-id="4d984-141">By default it is local.</span></span> <span data-ttu-id="4d984-142">Ha a SaveToAdl jelszavát határozza meg, akkor ez egy ADL-útvonal ugyanazon fiókban</span><span class="sxs-lookup"><span data-stu-id="4d984-142">If SaveToAdl is pecified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="4d984-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d984-143">-PassThru</span></span>
<span data-ttu-id="4d984-144">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4d984-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="4d984-145">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="4d984-145">-Path</span></span>
<span data-ttu-id="4d984-146">A megadott adattó-fiók útvonala, amelyet le kell olvasnia.</span><span class="sxs-lookup"><span data-stu-id="4d984-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="4d984-147">A "/Folder/file.txt" formátumban lehet fájl vagy mappa, ahol az első "/" a DNS a fájlrendszer gyökerét jelzi.</span><span class="sxs-lookup"><span data-stu-id="4d984-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="4d984-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="4d984-148">-SaveToAdl</span></span>
<span data-ttu-id="4d984-149">Ha a továbbítás után menti a memóriaképfájl-fájlt az ADL-ra.</span><span class="sxs-lookup"><span data-stu-id="4d984-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="4d984-150">A DumpFile wil egy ADL-útvonal, abban az esetben</span><span class="sxs-lookup"><span data-stu-id="4d984-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="4d984-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d984-151">-Confirm</span></span>
<span data-ttu-id="4d984-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d984-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d984-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d984-153">-WhatIf</span></span>
<span data-ttu-id="4d984-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d984-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d984-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d984-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d984-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d984-156">CommonParameters</span></span>
<span data-ttu-id="4d984-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d984-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d984-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d984-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d984-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d984-159">INPUTS</span></span>

### <span data-ttu-id="4d984-160">System. String</span><span class="sxs-lookup"><span data-stu-id="4d984-160">System.String</span></span>

### <span data-ttu-id="4d984-161">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4d984-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4d984-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d984-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4d984-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4d984-163">System.Int32</span></span>

## <span data-ttu-id="4d984-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d984-164">OUTPUTS</span></span>

### <span data-ttu-id="4d984-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d984-165">System.Boolean</span></span>

## <span data-ttu-id="4d984-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d984-166">NOTES</span></span>

## <span data-ttu-id="4d984-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d984-167">RELATED LINKS</span></span>
