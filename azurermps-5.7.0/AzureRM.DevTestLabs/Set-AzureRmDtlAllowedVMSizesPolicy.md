---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: e1c5fad70147300bb08fdafb94fb81079a02ea00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494504"
---
# <span data-ttu-id="9b6cf-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="9b6cf-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="9b6cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6cf-103">Az engedélyezett virtuálisgép-méretekre vonatkozó házirendet állítja be a DevTest Labs-ban.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b6cf-104">SYNTAX</span></span>

### <span data-ttu-id="9b6cf-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b6cf-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b6cf-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="9b6cf-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b6cf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b6cf-107">DESCRIPTION</span></span>
<span data-ttu-id="9b6cf-108">A **set-AzureRmDtlAllowedVMSizesPolicy** parancsmag az engedélyezett virtuálisgép-méretekre vonatkozó házirendet adja meg, amely a laboratóriumban engedélyezett virtuális gépek méreteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="9b6cf-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="9b6cf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9b6cf-110">EXAMPLES</span></span>

## <span data-ttu-id="9b6cf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b6cf-111">PARAMETERS</span></span>

### <span data-ttu-id="9b6cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6cf-112">-DefaultProfile</span></span>
<span data-ttu-id="9b6cf-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9b6cf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="9b6cf-114">-Disable</span></span>
<span data-ttu-id="9b6cf-115">Jelzi, hogy ez a parancsmag letiltja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="9b6cf-116">-Enable</span></span>
<span data-ttu-id="9b6cf-117">Jelzi, hogy ez a parancsmag engedélyezi a házirendet.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="9b6cf-118">-LabName</span></span>
<span data-ttu-id="9b6cf-119">Annak a laboratóriumnak a neve, amelyhez a parancsmag a virtuális gép méretére vonatkozó házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="9b6cf-121">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="9b6cf-122">-VmSizes</span></span>
<span data-ttu-id="9b6cf-123">Karakterláncként adja meg a laboratóriumban engedélyezett virtuális számítógép-méretek listáját.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b6cf-124">-Confirm</span></span>
<span data-ttu-id="9b6cf-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6cf-126">-WhatIf</span></span>
<span data-ttu-id="9b6cf-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b6cf-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6cf-129">CommonParameters</span></span>
<span data-ttu-id="9b6cf-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b6cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6cf-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6cf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6cf-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b6cf-132">INPUTS</span></span>

### <span data-ttu-id="9b6cf-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="9b6cf-133">None</span></span>
<span data-ttu-id="9b6cf-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b6cf-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b6cf-135">OUTPUTS</span></span>

### <span data-ttu-id="9b6cf-136">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9b6cf-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="9b6cf-137">Ez a parancsmag azt a házirendet adja eredményül, amely a laboratóriumban engedélyezett virtuális gépek méretének listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b6cf-137">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="9b6cf-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b6cf-138">NOTES</span></span>

## <span data-ttu-id="9b6cf-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b6cf-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b6cf-140">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="9b6cf-140">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


