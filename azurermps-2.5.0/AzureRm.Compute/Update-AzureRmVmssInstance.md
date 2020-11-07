---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
ms.openlocfilehash: 07b068587848bc8af92fc49b039155c0a2c4fdd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850037"
---
# <span data-ttu-id="1ce81-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="1ce81-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="1ce81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ce81-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce81-103">Elindítja a VMSS példány manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="1ce81-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ce81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ce81-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce81-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ce81-105">DESCRIPTION</span></span>
<span data-ttu-id="1ce81-106">Az Update-AzureRmVmssInstance parancsmag a megadott virtuálisgép-készlet (VMSS-példány) kézi frissítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="1ce81-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="1ce81-107">Ezt a beállítást akkor használja a rendszer, ha a VMSS-méretarány beállítása beállítás manuális értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="1ce81-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="1ce81-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1ce81-108">EXAMPLES</span></span>

### <span data-ttu-id="1ce81-109">Példa 1: a VMSS példány frissítésének megkezdése</span><span class="sxs-lookup"><span data-stu-id="1ce81-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="1ce81-110">Ez a parancs elindítja a VMScaleSet001 nevű VMSS frissítését, amelynek a példány azonosítója 0.</span><span class="sxs-lookup"><span data-stu-id="1ce81-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="1ce81-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ce81-111">PARAMETERS</span></span>

### <span data-ttu-id="1ce81-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ce81-112">-AsJob</span></span>
<span data-ttu-id="1ce81-113">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="1ce81-113">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce81-114">-DefaultProfile</span></span>
<span data-ttu-id="1ce81-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ce81-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce81-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1ce81-116">-InstanceId</span></span>
<span data-ttu-id="1ce81-117">Karakterláncként adja meg a frissítendő példány AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="1ce81-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce81-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ce81-119">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ce81-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="1ce81-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1ce81-120">-VMScaleSetName</span></span>
<span data-ttu-id="1ce81-121">Annak a VMSS-példánynak a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="1ce81-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ce81-122">-Confirm</span></span>
<span data-ttu-id="1ce81-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ce81-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce81-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce81-124">-WhatIf</span></span>
<span data-ttu-id="1ce81-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ce81-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1ce81-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ce81-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce81-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce81-127">CommonParameters</span></span>
<span data-ttu-id="1ce81-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ce81-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce81-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce81-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce81-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ce81-130">INPUTS</span></span>

### <span data-ttu-id="1ce81-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="1ce81-131">None</span></span>
<span data-ttu-id="1ce81-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1ce81-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ce81-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ce81-133">OUTPUTS</span></span>

###  
<span data-ttu-id="1ce81-134">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1ce81-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1ce81-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ce81-135">NOTES</span></span>

## <span data-ttu-id="1ce81-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ce81-136">RELATED LINKS</span></span>

[<span data-ttu-id="1ce81-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1ce81-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


