---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 459ae0e3d18056c6579d4fd6248548155e1471cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495372"
---
# <span data-ttu-id="60181-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="60181-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="60181-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60181-102">SYNOPSIS</span></span>
<span data-ttu-id="60181-103">A DevTest Labs-ban egy Lab virtuális gép felhasználónként házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="60181-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60181-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60181-104">SYNTAX</span></span>

### <span data-ttu-id="60181-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60181-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60181-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="60181-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60181-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="60181-107">DESCRIPTION</span></span>
<span data-ttu-id="60181-108">A **set-AzureRmDtlVMsPerUserPolicy** parancsmag egy Lab virtuális gép felhasználónként való beállítását állítja be, amely a felhasználónként engedélyezett virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="60181-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="60181-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="60181-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="60181-110">Példák</span><span class="sxs-lookup"><span data-stu-id="60181-110">EXAMPLES</span></span>

## <span data-ttu-id="60181-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60181-111">PARAMETERS</span></span>

### <span data-ttu-id="60181-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60181-112">-DefaultProfile</span></span>
<span data-ttu-id="60181-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="60181-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60181-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="60181-114">-Disable</span></span>
<span data-ttu-id="60181-115">Jelzi, hogy ez a parancsmag letiltja a Lab házirendet.</span><span class="sxs-lookup"><span data-stu-id="60181-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="60181-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="60181-116">-Enable</span></span>
<span data-ttu-id="60181-117">Azt jelzi, hogy ez a parancsmag engedélyezi a Lab házirendet.</span><span class="sxs-lookup"><span data-stu-id="60181-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="60181-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="60181-118">-LabName</span></span>
<span data-ttu-id="60181-119">Annak a laboratóriumnak a nevét adja meg, amelynek a parancsmagja a virtuális gépek felhasználónkénti házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="60181-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="60181-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="60181-120">-MaxVMs</span></span>
<span data-ttu-id="60181-121">A laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="60181-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60181-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60181-122">-ResourceGroupName</span></span>
<span data-ttu-id="60181-123">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="60181-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="60181-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60181-124">-Confirm</span></span>
<span data-ttu-id="60181-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60181-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60181-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60181-126">-WhatIf</span></span>
<span data-ttu-id="60181-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60181-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60181-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60181-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60181-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60181-129">CommonParameters</span></span>
<span data-ttu-id="60181-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60181-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60181-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60181-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60181-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60181-132">INPUTS</span></span>

### <span data-ttu-id="60181-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="60181-133">None</span></span>
<span data-ttu-id="60181-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="60181-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60181-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60181-135">OUTPUTS</span></span>

### <span data-ttu-id="60181-136">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="60181-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="60181-137">Ez a parancsmag azt a házirendet adja eredményül, amely megadja a laboratóriumban egy felhasználó által létrehozható virtuális gépek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="60181-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="60181-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60181-138">NOTES</span></span>

## <span data-ttu-id="60181-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60181-139">RELATED LINKS</span></span>

[<span data-ttu-id="60181-140">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="60181-140">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


