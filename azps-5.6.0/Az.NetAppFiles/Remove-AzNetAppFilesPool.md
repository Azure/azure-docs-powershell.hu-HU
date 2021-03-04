---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: a62e6093ec5cfdf7244ea83b2dccf07ad07308fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926777"
---
# <span data-ttu-id="db36a-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="db36a-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="db36a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db36a-102">SYNOPSIS</span></span>
<span data-ttu-id="db36a-103">Azure NetApp-fájlok (ANF-) készlet törlése.</span><span class="sxs-lookup"><span data-stu-id="db36a-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="db36a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db36a-104">SYNTAX</span></span>

### <span data-ttu-id="db36a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db36a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db36a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db36a-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db36a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db36a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db36a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db36a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db36a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db36a-109">DESCRIPTION</span></span>
<span data-ttu-id="db36a-110">A **Remove-AzNetAppFilesPool** parancsmag törli az ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="db36a-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="db36a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db36a-111">EXAMPLES</span></span>

### <span data-ttu-id="db36a-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="db36a-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="db36a-113">Ez a parancs törli a "MyAnfPool" ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="db36a-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="db36a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db36a-114">PARAMETERS</span></span>

### <span data-ttu-id="db36a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="db36a-115">-AccountName</span></span>
<span data-ttu-id="db36a-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="db36a-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="db36a-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="db36a-117">-AccountObject</span></span>
<span data-ttu-id="db36a-118">Az eltávolítható készletet tartalmazó fiókobjektum</span><span class="sxs-lookup"><span data-stu-id="db36a-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db36a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db36a-119">-DefaultProfile</span></span>
<span data-ttu-id="db36a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db36a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db36a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db36a-121">-InputObject</span></span>
<span data-ttu-id="db36a-122">Az eltávolítható készletobjektum</span><span class="sxs-lookup"><span data-stu-id="db36a-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db36a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="db36a-123">-Name</span></span>
<span data-ttu-id="db36a-124">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="db36a-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db36a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db36a-125">-PassThru</span></span>
<span data-ttu-id="db36a-126">Annak visszaadése, hogy a megadott készlet eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="db36a-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="db36a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db36a-127">-ResourceGroupName</span></span>
<span data-ttu-id="db36a-128">Az ANF-készlet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="db36a-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="db36a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db36a-129">-ResourceId</span></span>
<span data-ttu-id="db36a-130">Az ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="db36a-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="db36a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db36a-131">-Confirm</span></span>
<span data-ttu-id="db36a-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db36a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db36a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db36a-133">-WhatIf</span></span>
<span data-ttu-id="db36a-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db36a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db36a-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db36a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db36a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db36a-136">CommonParameters</span></span>
<span data-ttu-id="db36a-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db36a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db36a-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db36a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db36a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db36a-139">INPUTS</span></span>

### <span data-ttu-id="db36a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="db36a-140">System.String</span></span>

### <span data-ttu-id="db36a-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="db36a-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="db36a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="db36a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="db36a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db36a-143">OUTPUTS</span></span>

### <span data-ttu-id="db36a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db36a-144">System.Boolean</span></span>

## <span data-ttu-id="db36a-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db36a-145">NOTES</span></span>

## <span data-ttu-id="db36a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db36a-146">RELATED LINKS</span></span>
