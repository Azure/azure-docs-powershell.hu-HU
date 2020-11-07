---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: cd51835c2ca5a228e2eb3a54a4b3a724505e9d7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667151"
---
# <span data-ttu-id="b3f21-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="b3f21-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="b3f21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3f21-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f21-103">Elindítja a VMSS példány manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="b3f21-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="b3f21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3f21-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3f21-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3f21-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f21-106">Az Update-AzVmssInstance parancsmag a megadott virtuálisgép-készlet (VMSS-példány) kézi frissítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="b3f21-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="b3f21-107">Ezt a beállítást akkor használja a rendszer, ha a VMSS-méretarány beállítása beállítás manuális értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="b3f21-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="b3f21-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b3f21-108">EXAMPLES</span></span>

### <span data-ttu-id="b3f21-109">Példa 1: a VMSS példány frissítésének megkezdése</span><span class="sxs-lookup"><span data-stu-id="b3f21-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="b3f21-110">Ez a parancs elindítja a VMScaleSet001 nevű VMSS frissítését, amelynek a példány azonosítója 0.</span><span class="sxs-lookup"><span data-stu-id="b3f21-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="b3f21-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3f21-111">PARAMETERS</span></span>

### <span data-ttu-id="b3f21-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3f21-112">-AsJob</span></span>
<span data-ttu-id="b3f21-113">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="b3f21-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3f21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f21-114">-DefaultProfile</span></span>
<span data-ttu-id="b3f21-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3f21-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3f21-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b3f21-116">-InstanceId</span></span>
<span data-ttu-id="b3f21-117">Karakterláncként adja meg a frissítendő példány AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="b3f21-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f21-118">-ResourceGroupName</span></span>
<span data-ttu-id="b3f21-119">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3f21-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b3f21-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b3f21-120">-VMScaleSetName</span></span>
<span data-ttu-id="b3f21-121">Annak a VMSS-példánynak a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="b3f21-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f21-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3f21-122">-Confirm</span></span>
<span data-ttu-id="b3f21-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3f21-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f21-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f21-124">-WhatIf</span></span>
<span data-ttu-id="b3f21-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3f21-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f21-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3f21-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f21-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f21-127">CommonParameters</span></span>
<span data-ttu-id="b3f21-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3f21-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f21-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b3f21-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f21-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3f21-130">INPUTS</span></span>

### <span data-ttu-id="b3f21-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b3f21-131">System.String</span></span>

### <span data-ttu-id="b3f21-132">System. string []</span><span class="sxs-lookup"><span data-stu-id="b3f21-132">System.String[]</span></span>

## <span data-ttu-id="b3f21-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3f21-133">OUTPUTS</span></span>

### <span data-ttu-id="b3f21-134">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b3f21-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b3f21-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3f21-135">NOTES</span></span>

## <span data-ttu-id="b3f21-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3f21-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3f21-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3f21-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


