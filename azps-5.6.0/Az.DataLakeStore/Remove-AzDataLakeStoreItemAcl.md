---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9b762a2fe0f12483fd664b8862e483b1b948bc75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928178"
---
# <span data-ttu-id="94d06-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="94d06-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="94d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d06-102">SYNOPSIS</span></span>
<span data-ttu-id="94d06-103">Törli a Data Lake Store-ban tárolt fájl vagy mappa ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="94d06-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="94d06-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94d06-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d06-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94d06-105">DESCRIPTION</span></span>
<span data-ttu-id="94d06-106">A **Remove-AzDataLakeStoreItemAcl** parancsmag törli egy adattavatárban lévő fájl vagy mappa hozzáférés-vezérlési listáját (ACL).</span><span class="sxs-lookup"><span data-stu-id="94d06-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="94d06-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94d06-107">EXAMPLES</span></span>

### <span data-ttu-id="94d06-108">1. példa: Az ACL eltávolítása egy mappából</span><span class="sxs-lookup"><span data-stu-id="94d06-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="94d06-109">Ez a parancs eltávolítja a ContosoADL-fiók gyökérkönyvtárának ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="94d06-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="94d06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d06-110">PARAMETERS</span></span>

### <span data-ttu-id="94d06-111">-Account</span><span class="sxs-lookup"><span data-stu-id="94d06-111">-Account</span></span>
<span data-ttu-id="94d06-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94d06-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="94d06-113">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="94d06-113">-Default</span></span>
<span data-ttu-id="94d06-114">Azt jelzi, hogy a parancsmag eltávolítja egy fájl vagy mappa alapértelmezett ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="94d06-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="94d06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d06-115">-DefaultProfile</span></span>
<span data-ttu-id="94d06-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94d06-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d06-117">-Force</span><span class="sxs-lookup"><span data-stu-id="94d06-117">-Force</span></span>
<span data-ttu-id="94d06-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="94d06-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94d06-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94d06-119">-PassThru</span></span>
<span data-ttu-id="94d06-120">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="94d06-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="94d06-121">-Path</span><span class="sxs-lookup"><span data-stu-id="94d06-121">-Path</span></span>
<span data-ttu-id="94d06-122">Az elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="94d06-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="94d06-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94d06-123">-Confirm</span></span>
<span data-ttu-id="94d06-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94d06-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d06-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d06-125">-WhatIf</span></span>
<span data-ttu-id="94d06-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94d06-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d06-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94d06-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d06-128">CommonParameters</span></span>
<span data-ttu-id="94d06-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d06-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d06-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d06-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94d06-131">INPUTS</span></span>

### <span data-ttu-id="94d06-132">System.String</span><span class="sxs-lookup"><span data-stu-id="94d06-132">System.String</span></span>

### <span data-ttu-id="94d06-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="94d06-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="94d06-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94d06-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="94d06-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94d06-135">OUTPUTS</span></span>

### <span data-ttu-id="94d06-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94d06-136">System.Boolean</span></span>

## <span data-ttu-id="94d06-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94d06-137">NOTES</span></span>
* <span data-ttu-id="94d06-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="94d06-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="94d06-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94d06-139">RELATED LINKS</span></span>

[<span data-ttu-id="94d06-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="94d06-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="94d06-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="94d06-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="94d06-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="94d06-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


