---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025637"
---
# <span data-ttu-id="fd8ad-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fd8ad-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="fd8ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8ad-103">Azure NetApp-fájlok (ANF-) készletének törlése.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="fd8ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd8ad-104">SYNTAX</span></span>

### <span data-ttu-id="fd8ad-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd8ad-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd8ad-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8ad-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd8ad-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8ad-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd8ad-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd8ad-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd8ad-109">DESCRIPTION</span></span>
<span data-ttu-id="fd8ad-110">A **Remove-AzNetAppFilesPool** parancsmag törli a ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="fd8ad-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fd8ad-111">EXAMPLES</span></span>

### <span data-ttu-id="fd8ad-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd8ad-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="fd8ad-113">Ez a parancs törli a "MyAnfPool" ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="fd8ad-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd8ad-114">PARAMETERS</span></span>

### <span data-ttu-id="fd8ad-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd8ad-115">-AccountName</span></span>
<span data-ttu-id="fd8ad-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="fd8ad-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="fd8ad-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="fd8ad-117">-AccountObject</span></span>
<span data-ttu-id="fd8ad-118">Az eltávolítandó készletet tartalmazó ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="fd8ad-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="fd8ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8ad-119">-DefaultProfile</span></span>
<span data-ttu-id="fd8ad-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd8ad-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd8ad-121">-InputObject</span></span>
<span data-ttu-id="fd8ad-122">Az eltávolítandó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="fd8ad-122">The pool object to remove</span></span>

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

### <span data-ttu-id="fd8ad-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd8ad-123">-Name</span></span>
<span data-ttu-id="fd8ad-124">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="fd8ad-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="fd8ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd8ad-125">-PassThru</span></span>
<span data-ttu-id="fd8ad-126">A megadott alkalmazáskészlet sikeres eltávolításának visszavonása</span><span class="sxs-lookup"><span data-stu-id="fd8ad-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="fd8ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd8ad-128">A ANF-készlet erőforráscsoport csoportja</span><span class="sxs-lookup"><span data-stu-id="fd8ad-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="fd8ad-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd8ad-129">-ResourceId</span></span>
<span data-ttu-id="fd8ad-130">A ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fd8ad-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="fd8ad-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd8ad-131">-Confirm</span></span>
<span data-ttu-id="fd8ad-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8ad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8ad-133">-WhatIf</span></span>
<span data-ttu-id="fd8ad-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8ad-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8ad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8ad-136">CommonParameters</span></span>
<span data-ttu-id="fd8ad-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd8ad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8ad-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fd8ad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8ad-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd8ad-139">INPUTS</span></span>

### <span data-ttu-id="fd8ad-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fd8ad-140">System.String</span></span>

### <span data-ttu-id="fd8ad-141">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="fd8ad-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="fd8ad-142">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fd8ad-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="fd8ad-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd8ad-143">OUTPUTS</span></span>

### <span data-ttu-id="fd8ad-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd8ad-144">System.Boolean</span></span>

## <span data-ttu-id="fd8ad-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd8ad-145">NOTES</span></span>

## <span data-ttu-id="fd8ad-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd8ad-146">RELATED LINKS</span></span>
