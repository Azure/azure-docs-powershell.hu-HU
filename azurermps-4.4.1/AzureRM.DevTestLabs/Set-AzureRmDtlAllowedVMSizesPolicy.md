---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8248c5ef5e4de2ab945d7f5f39dd4eea6defdf8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679448"
---
# <span data-ttu-id="028d2-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="028d2-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="028d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="028d2-102">SYNOPSIS</span></span>
<span data-ttu-id="028d2-103">Az engedélyezett virtuálisgép-méretekre vonatkozó házirendet állítja be a DevTest Labs-ban.</span><span class="sxs-lookup"><span data-stu-id="028d2-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="028d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="028d2-104">SYNTAX</span></span>

### <span data-ttu-id="028d2-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="028d2-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="028d2-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="028d2-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="028d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="028d2-107">DESCRIPTION</span></span>
<span data-ttu-id="028d2-108">A **set-AzureRmDtlAllowedVMSizesPolicy** parancsmag az engedélyezett virtuálisgép-méretekre vonatkozó házirendet adja meg, amely a laboratóriumban engedélyezett virtuális gépek méreteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="028d2-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="028d2-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="028d2-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="028d2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="028d2-110">EXAMPLES</span></span>

## <span data-ttu-id="028d2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="028d2-111">PARAMETERS</span></span>

### <span data-ttu-id="028d2-112">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="028d2-112">-Disable</span></span>
<span data-ttu-id="028d2-113">Jelzi, hogy ez a parancsmag letiltja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="028d2-113">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028d2-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="028d2-114">-Enable</span></span>
<span data-ttu-id="028d2-115">Jelzi, hogy ez a parancsmag engedélyezi a házirendet.</span><span class="sxs-lookup"><span data-stu-id="028d2-115">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028d2-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="028d2-116">-LabName</span></span>
<span data-ttu-id="028d2-117">Annak a laboratóriumnak a neve, amelyhez a parancsmag a virtuális gép méretére vonatkozó házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="028d2-117">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="028d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="028d2-119">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="028d2-119">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028d2-120">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="028d2-120">-VmSizes</span></span>
<span data-ttu-id="028d2-121">Karakterláncként adja meg a laboratóriumban engedélyezett virtuális számítógép-méretek listáját.</span><span class="sxs-lookup"><span data-stu-id="028d2-121">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028d2-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="028d2-122">-Confirm</span></span>
<span data-ttu-id="028d2-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="028d2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="028d2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="028d2-124">-WhatIf</span></span>
<span data-ttu-id="028d2-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="028d2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="028d2-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="028d2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="028d2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028d2-127">-DefaultProfile</span></span>
<span data-ttu-id="028d2-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="028d2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028d2-129">CommonParameters</span></span>
<span data-ttu-id="028d2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="028d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028d2-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="028d2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028d2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="028d2-132">INPUTS</span></span>

## <span data-ttu-id="028d2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="028d2-133">OUTPUTS</span></span>

### <span data-ttu-id="028d2-134">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="028d2-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="028d2-135">Ez a parancsmag azt a házirendet adja eredményül, amely a laboratóriumban engedélyezett virtuális gépek méretének listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="028d2-135">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="028d2-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="028d2-136">NOTES</span></span>

## <span data-ttu-id="028d2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="028d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="028d2-138">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="028d2-138">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


