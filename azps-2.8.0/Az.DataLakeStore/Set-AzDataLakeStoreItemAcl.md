---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 53cf81c4996a9d77d1452ffd6d5f99c111aecbf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666805"
---
# <span data-ttu-id="af67c-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="af67c-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="af67c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af67c-102">SYNOPSIS</span></span>
<span data-ttu-id="af67c-103">Módosítja az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="af67c-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="af67c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af67c-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af67c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af67c-105">DESCRIPTION</span></span>
<span data-ttu-id="af67c-106">A **set-AzDataLakeStoreItemAcl** parancsmag az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési LISTÁJÁT (ACL) módosítja.</span><span class="sxs-lookup"><span data-stu-id="af67c-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="af67c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af67c-107">EXAMPLES</span></span>

### <span data-ttu-id="af67c-108">Példa 1: fájlok és mappák ACL-beállítása</span><span class="sxs-lookup"><span data-stu-id="af67c-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="af67c-109">Az első parancs beolvassa az ContosoADL-fiók gyökérkönyvtárát, majd a $ACL változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="af67c-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="af67c-110">A második parancs a $ACL elérési Test.txt a fájlhoz tartozó hozzáférés-vezérlési beállításokkal.</span><span class="sxs-lookup"><span data-stu-id="af67c-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="af67c-111">2. példa: a mappa rekurzív módon való HOZZÁFÉRÉSének beállítása</span><span class="sxs-lookup"><span data-stu-id="af67c-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="af67c-112">Az első parancs megkapja az ContosoADL-fiók címtár-Mappa1 tartozó ACL-t, majd a $ACL változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="af67c-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="af67c-113">A második parancs az ACL-t a Mappa2-ra, a hozzá tartozó alkönyvtárakra és-fájlokra állítja be $ACL-ban.</span><span class="sxs-lookup"><span data-stu-id="af67c-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="af67c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af67c-114">PARAMETERS</span></span>

### <span data-ttu-id="af67c-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="af67c-115">-Account</span></span>
<span data-ttu-id="af67c-116">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af67c-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="af67c-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="af67c-117">-Acl</span></span>
<span data-ttu-id="af67c-118">Egy fájl vagy mappa hozzáférés-vezérlési listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="af67c-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af67c-119">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="af67c-119">-Concurrency</span></span>
<span data-ttu-id="af67c-120">A párhuzamosan feldolgozott fájlok/könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="af67c-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="af67c-121">Nem kötelező: az alapértelmezett beállítás lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="af67c-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="af67c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af67c-122">-DefaultProfile</span></span>
<span data-ttu-id="af67c-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af67c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af67c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af67c-124">-PassThru</span></span>
<span data-ttu-id="af67c-125">Jelzi, hogy az eredményül kapott ACL-t vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="af67c-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="af67c-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="af67c-126">-Path</span></span>
<span data-ttu-id="af67c-127">A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="af67c-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="af67c-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="af67c-128">-Recurse</span></span>
<span data-ttu-id="af67c-129">Azt jelzi, hogy az ACL-t a program rekurzív módon adja meg a alárendelt alkönyvtárak és fájlok számára.</span><span class="sxs-lookup"><span data-stu-id="af67c-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="af67c-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="af67c-130">-ShowProgress</span></span>
<span data-ttu-id="af67c-131">Ha a betelt, akkor a folyamat állapota látható.</span><span class="sxs-lookup"><span data-stu-id="af67c-131">If passed then progress status is showed.</span></span> <span data-ttu-id="af67c-132">Csak akkor érvényes, ha a rekurzív ACL-készlet készen van.</span><span class="sxs-lookup"><span data-stu-id="af67c-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="af67c-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af67c-133">-Confirm</span></span>
<span data-ttu-id="af67c-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af67c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af67c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af67c-135">-WhatIf</span></span>
<span data-ttu-id="af67c-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af67c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af67c-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af67c-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af67c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af67c-138">CommonParameters</span></span>
<span data-ttu-id="af67c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af67c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af67c-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af67c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af67c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af67c-141">INPUTS</span></span>

### <span data-ttu-id="af67c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="af67c-142">System.String</span></span>

### <span data-ttu-id="af67c-143">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="af67c-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="af67c-144">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="af67c-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="af67c-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af67c-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="af67c-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="af67c-146">System.Int32</span></span>

## <span data-ttu-id="af67c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af67c-147">OUTPUTS</span></span>

### <span data-ttu-id="af67c-148">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="af67c-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="af67c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af67c-149">NOTES</span></span>

## <span data-ttu-id="af67c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af67c-150">RELATED LINKS</span></span>
