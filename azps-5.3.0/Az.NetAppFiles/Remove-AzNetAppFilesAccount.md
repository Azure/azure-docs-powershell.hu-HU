---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480019"
---
# <span data-ttu-id="e0753-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e0753-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="e0753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0753-102">SYNOPSIS</span></span>
<span data-ttu-id="e0753-103">Töröl egy Azure NetApp-fájlt (ANF-fiókot).</span><span class="sxs-lookup"><span data-stu-id="e0753-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="e0753-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0753-104">SYNTAX</span></span>

### <span data-ttu-id="e0753-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0753-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0753-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0753-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0753-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0753-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0753-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0753-108">DESCRIPTION</span></span>
<span data-ttu-id="e0753-109">A **Remove-AzNetAppFilesAccount** parancsmag töröl egy ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="e0753-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="e0753-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0753-110">EXAMPLES</span></span>

### <span data-ttu-id="e0753-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0753-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="e0753-112">Ez a parancs törli a "MyAnfAccount" ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="e0753-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="e0753-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0753-113">PARAMETERS</span></span>

### <span data-ttu-id="e0753-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0753-114">-DefaultProfile</span></span>
<span data-ttu-id="e0753-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0753-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0753-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0753-116">-InputObject</span></span>
<span data-ttu-id="e0753-117">Az eltávolítható fiókobjektum</span><span class="sxs-lookup"><span data-stu-id="e0753-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0753-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e0753-118">-Name</span></span>
<span data-ttu-id="e0753-119">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="e0753-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0753-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0753-120">-PassThru</span></span>
<span data-ttu-id="e0753-121">Annak visszaadése, hogy a megadott fiók eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="e0753-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="e0753-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0753-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0753-123">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="e0753-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0753-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0753-124">-ResourceId</span></span>
<span data-ttu-id="e0753-125">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e0753-125">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0753-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0753-126">-Confirm</span></span>
<span data-ttu-id="e0753-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e0753-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0753-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0753-128">-WhatIf</span></span>
<span data-ttu-id="e0753-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e0753-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0753-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0753-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0753-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0753-131">CommonParameters</span></span>
<span data-ttu-id="e0753-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0753-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0753-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0753-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0753-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0753-134">INPUTS</span></span>

### <span data-ttu-id="e0753-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e0753-135">System.String</span></span>

### <span data-ttu-id="e0753-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e0753-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e0753-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0753-137">OUTPUTS</span></span>

### <span data-ttu-id="e0753-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0753-138">System.Boolean</span></span>

## <span data-ttu-id="e0753-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0753-139">NOTES</span></span>

## <span data-ttu-id="e0753-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0753-140">RELATED LINKS</span></span>
