---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187284"
---
# <span data-ttu-id="e8118-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e8118-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="e8118-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8118-102">SYNOPSIS</span></span>
<span data-ttu-id="e8118-103">Azure NetApp-fájlok (ANF-) készletének törlése.</span><span class="sxs-lookup"><span data-stu-id="e8118-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="e8118-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8118-104">SYNTAX</span></span>

### <span data-ttu-id="e8118-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8118-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8118-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8118-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8118-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8118-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8118-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8118-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8118-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8118-109">DESCRIPTION</span></span>
<span data-ttu-id="e8118-110">A **Remove-AzNetAppFilesPool** parancsmag törli a ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="e8118-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="e8118-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e8118-111">EXAMPLES</span></span>

### <span data-ttu-id="e8118-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8118-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="e8118-113">Ez a parancs törli a "MyAnfPool" ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="e8118-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="e8118-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8118-114">PARAMETERS</span></span>

### <span data-ttu-id="e8118-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8118-115">-AccountName</span></span>
<span data-ttu-id="e8118-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="e8118-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="e8118-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e8118-117">-AccountObject</span></span>
<span data-ttu-id="e8118-118">Az eltávolítandó készletet tartalmazó ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="e8118-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="e8118-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8118-119">-DefaultProfile</span></span>
<span data-ttu-id="e8118-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8118-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8118-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8118-121">-InputObject</span></span>
<span data-ttu-id="e8118-122">Az eltávolítandó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="e8118-122">The pool object to remove</span></span>

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

### <span data-ttu-id="e8118-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8118-123">-Name</span></span>
<span data-ttu-id="e8118-124">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="e8118-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="e8118-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8118-125">-PassThru</span></span>
<span data-ttu-id="e8118-126">A megadott alkalmazáskészlet sikeres eltávolításának visszavonása</span><span class="sxs-lookup"><span data-stu-id="e8118-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="e8118-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8118-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8118-128">A ANF-készlet erőforráscsoport csoportja</span><span class="sxs-lookup"><span data-stu-id="e8118-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="e8118-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8118-129">-ResourceId</span></span>
<span data-ttu-id="e8118-130">A ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e8118-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="e8118-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8118-131">-Confirm</span></span>
<span data-ttu-id="e8118-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8118-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8118-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8118-133">-WhatIf</span></span>
<span data-ttu-id="e8118-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8118-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8118-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8118-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8118-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8118-136">CommonParameters</span></span>
<span data-ttu-id="e8118-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8118-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8118-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8118-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8118-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8118-139">INPUTS</span></span>

### <span data-ttu-id="e8118-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e8118-140">System.String</span></span>

### <span data-ttu-id="e8118-141">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e8118-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="e8118-142">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e8118-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e8118-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8118-143">OUTPUTS</span></span>

### <span data-ttu-id="e8118-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8118-144">System.Boolean</span></span>

## <span data-ttu-id="e8118-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8118-145">NOTES</span></span>

## <span data-ttu-id="e8118-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8118-146">RELATED LINKS</span></span>
