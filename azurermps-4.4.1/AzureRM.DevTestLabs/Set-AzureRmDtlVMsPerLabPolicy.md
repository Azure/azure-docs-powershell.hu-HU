---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 95908e6b0976baf2ce9f3c117f54a6f1552e4957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679446"
---
# <span data-ttu-id="4e456-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="4e456-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="4e456-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e456-102">SYNOPSIS</span></span>
<span data-ttu-id="4e456-103">A DevTest Labs-ban egy Lab virtuális számítógépekre vonatkozó házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="4e456-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e456-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e456-104">SYNTAX</span></span>

### <span data-ttu-id="4e456-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e456-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e456-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="4e456-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e456-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e456-107">DESCRIPTION</span></span>
<span data-ttu-id="4e456-108">A **set-AzureRmDtlVMsPerLabPolicy** parancsmag egy Lab virtuális számítógépeit állítja be, amely a laboratóriumban engedélyezett virtuális gépek teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e456-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="4e456-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="4e456-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="4e456-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4e456-110">EXAMPLES</span></span>

## <span data-ttu-id="4e456-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e456-111">PARAMETERS</span></span>

### <span data-ttu-id="4e456-112">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="4e456-112">-Disable</span></span>
<span data-ttu-id="4e456-113">Jelzi, hogy ez a parancsmag letiltja a Lab házirendjét.</span><span class="sxs-lookup"><span data-stu-id="4e456-113">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="4e456-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="4e456-114">-Enable</span></span>
<span data-ttu-id="4e456-115">Jelzi, hogy ez a parancsmag engedélyezi a Lab házirendjét.</span><span class="sxs-lookup"><span data-stu-id="4e456-115">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="4e456-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="4e456-116">-LabName</span></span>
<span data-ttu-id="4e456-117">Annak a laboratóriumnak a nevét adja meg, amelynek a parancsmagja a virtuális gépeket egy Lab-házirend szerint állítja be.</span><span class="sxs-lookup"><span data-stu-id="4e456-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="4e456-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="4e456-118">-MaxVMs</span></span>
<span data-ttu-id="4e456-119">A laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e456-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e456-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e456-120">-ResourceGroupName</span></span>
<span data-ttu-id="4e456-121">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="4e456-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="4e456-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e456-122">-Confirm</span></span>
<span data-ttu-id="4e456-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e456-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e456-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e456-124">-WhatIf</span></span>
<span data-ttu-id="4e456-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e456-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e456-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e456-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e456-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e456-127">-DefaultProfile</span></span>
<span data-ttu-id="4e456-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e456-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e456-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e456-129">CommonParameters</span></span>
<span data-ttu-id="4e456-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e456-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e456-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e456-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e456-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e456-132">INPUTS</span></span>

## <span data-ttu-id="4e456-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e456-133">OUTPUTS</span></span>

### <span data-ttu-id="4e456-134">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="4e456-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="4e456-135">Ez a parancsmag azt a házirendet adja eredményül, amely a laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e456-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="4e456-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e456-136">NOTES</span></span>

## <span data-ttu-id="4e456-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e456-137">RELATED LINKS</span></span>

[<span data-ttu-id="4e456-138">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="4e456-138">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


