---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165355"
---
# <span data-ttu-id="276b1-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="276b1-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="276b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="276b1-102">SYNOPSIS</span></span>
<span data-ttu-id="276b1-103">Törli a Data Lake Store-ban tárolt fájl vagy mappa ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="276b1-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="276b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="276b1-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="276b1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="276b1-105">DESCRIPTION</span></span>
<span data-ttu-id="276b1-106">A **Remove-AzDataLakeStoreItemAcl** parancsmag törli egy adattavatárban lévő fájl vagy mappa hozzáférés-vezérlési listáját (ACL).</span><span class="sxs-lookup"><span data-stu-id="276b1-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="276b1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="276b1-107">EXAMPLES</span></span>

### <span data-ttu-id="276b1-108">1. példa: Az ACL eltávolítása egy mappából</span><span class="sxs-lookup"><span data-stu-id="276b1-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="276b1-109">Ez a parancs eltávolítja a ContosoADL-fiók gyökérkönyvtárának ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="276b1-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="276b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="276b1-110">PARAMETERS</span></span>

### <span data-ttu-id="276b1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="276b1-111">-Account</span></span>
<span data-ttu-id="276b1-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="276b1-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="276b1-113">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="276b1-113">-Default</span></span>
<span data-ttu-id="276b1-114">Azt jelzi, hogy a parancsmag eltávolítja egy fájl vagy mappa alapértelmezett ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="276b1-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276b1-115">-DefaultProfile</span></span>
<span data-ttu-id="276b1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="276b1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="276b1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="276b1-117">-Force</span></span>
<span data-ttu-id="276b1-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="276b1-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276b1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="276b1-119">-PassThru</span></span>
<span data-ttu-id="276b1-120">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="276b1-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="276b1-121">-Path</span><span class="sxs-lookup"><span data-stu-id="276b1-121">-Path</span></span>
<span data-ttu-id="276b1-122">Az elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="276b1-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="276b1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="276b1-123">-Confirm</span></span>
<span data-ttu-id="276b1-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="276b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="276b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="276b1-125">-WhatIf</span></span>
<span data-ttu-id="276b1-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="276b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="276b1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="276b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="276b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276b1-128">CommonParameters</span></span>
<span data-ttu-id="276b1-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="276b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276b1-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276b1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276b1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="276b1-131">INPUTS</span></span>

### <span data-ttu-id="276b1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="276b1-132">System.String</span></span>

### <span data-ttu-id="276b1-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="276b1-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="276b1-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="276b1-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="276b1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="276b1-135">OUTPUTS</span></span>

### <span data-ttu-id="276b1-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="276b1-136">System.Boolean</span></span>

## <span data-ttu-id="276b1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="276b1-137">NOTES</span></span>
* <span data-ttu-id="276b1-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="276b1-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="276b1-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="276b1-139">RELATED LINKS</span></span>

[<span data-ttu-id="276b1-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="276b1-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="276b1-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="276b1-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="276b1-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="276b1-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


