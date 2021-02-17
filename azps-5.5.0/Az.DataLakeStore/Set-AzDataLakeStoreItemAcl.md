---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155818"
---
# <span data-ttu-id="b0f69-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b0f69-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="b0f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0f69-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f69-103">Módosítja a Data Lake Store-ban tárolt fájlok vagy mappák ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="b0f69-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b0f69-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0f69-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f69-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0f69-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f69-106">A **Set-AzDataLakeStoreItemAcl** parancsmag módosítja egy adattavatárban lévő fájl vagy mappa hozzáférés-vezérlési listáját (ACL).</span><span class="sxs-lookup"><span data-stu-id="b0f69-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b0f69-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0f69-107">EXAMPLES</span></span>

### <span data-ttu-id="b0f69-108">1. példa: Fájl és mappa ACL-ének beállítása</span><span class="sxs-lookup"><span data-stu-id="b0f69-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="b0f69-109">Az első parancs lekérte a ContosoADL-fiók gyökérkönyvtárának ACL-ét, majd tárolja azt a $ACL változóban.</span><span class="sxs-lookup"><span data-stu-id="b0f69-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="b0f69-110">A második parancs a fájl ACL-ét Test.txt a $ACL.</span><span class="sxs-lookup"><span data-stu-id="b0f69-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="b0f69-111">2. példa: A mappa rekurzív ACL-ének beállítása</span><span class="sxs-lookup"><span data-stu-id="b0f69-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="b0f69-112">Az első parancs lekérte a ContosoADL-fiók mappa1 mappájának ACL-ét, majd tárolja azt a $ACL változóban.</span><span class="sxs-lookup"><span data-stu-id="b0f69-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="b0f69-113">A második parancs az ACL-t rekurzívan a Folder2 mappára, altáraira és fájljaira állítja a $ACL.</span><span class="sxs-lookup"><span data-stu-id="b0f69-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="b0f69-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0f69-114">PARAMETERS</span></span>

### <span data-ttu-id="b0f69-115">-Account</span><span class="sxs-lookup"><span data-stu-id="b0f69-115">-Account</span></span>
<span data-ttu-id="b0f69-116">Az Adattavatár-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0f69-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b0f69-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="b0f69-117">-Acl</span></span>
<span data-ttu-id="b0f69-118">Egy fájl vagy mappa ACL-ét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0f69-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="b0f69-119">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="b0f69-119">-Concurrency</span></span>
<span data-ttu-id="b0f69-120">A párhuzamosan feldolgozott fájlok és könyvtárak száma.</span><span class="sxs-lookup"><span data-stu-id="b0f69-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="b0f69-121">Nem kötelező: egy észszerű alapértelmezett beállítás lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="b0f69-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="b0f69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f69-122">-DefaultProfile</span></span>
<span data-ttu-id="b0f69-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0f69-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0f69-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0f69-124">-PassThru</span></span>
<span data-ttu-id="b0f69-125">Azt jelzi, hogy az eredményül kapott ACL-t kell eredményül visszaadni.</span><span class="sxs-lookup"><span data-stu-id="b0f69-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="b0f69-126">-Path</span><span class="sxs-lookup"><span data-stu-id="b0f69-126">-Path</span></span>
<span data-ttu-id="b0f69-127">A fájl vagy mappa Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="b0f69-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b0f69-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b0f69-128">-Recurse</span></span>
<span data-ttu-id="b0f69-129">Azt jelzi, hogy az ACL-t rekurzív módon kell beállítani a gyermek alkönyvtárakhoz és fájlokhoz</span><span class="sxs-lookup"><span data-stu-id="b0f69-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="b0f69-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="b0f69-130">-ShowProgress</span></span>
<span data-ttu-id="b0f69-131">Ha a folyamat elért, akkor a folyamat állapota is 2010-et mutat.</span><span class="sxs-lookup"><span data-stu-id="b0f69-131">If passed then progress status is showed.</span></span> <span data-ttu-id="b0f69-132">Csak akkor alkalmazható, ha a rekurzív Acl halmaz kész.</span><span class="sxs-lookup"><span data-stu-id="b0f69-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="b0f69-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0f69-133">-Confirm</span></span>
<span data-ttu-id="b0f69-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0f69-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f69-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f69-135">-WhatIf</span></span>
<span data-ttu-id="b0f69-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0f69-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f69-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0f69-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f69-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f69-138">CommonParameters</span></span>
<span data-ttu-id="b0f69-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f69-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f69-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f69-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f69-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0f69-141">INPUTS</span></span>

### <span data-ttu-id="b0f69-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b0f69-142">System.String</span></span>

### <span data-ttu-id="b0f69-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b0f69-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b0f69-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="b0f69-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="b0f69-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0f69-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b0f69-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b0f69-146">System.Int32</span></span>

## <span data-ttu-id="b0f69-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0f69-147">OUTPUTS</span></span>

### <span data-ttu-id="b0f69-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="b0f69-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="b0f69-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0f69-149">NOTES</span></span>

## <span data-ttu-id="b0f69-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0f69-150">RELATED LINKS</span></span>
