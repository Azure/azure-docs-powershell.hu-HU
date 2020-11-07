---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: d8fb3b740a85b4cb258fcfa08bf9f4e06032fcb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842418"
---
# <span data-ttu-id="d5fe6-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="d5fe6-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="d5fe6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fe6-103">Elindítja a VMSS példány manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="d5fe6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5fe6-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5fe6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fe6-106">Az Update-AzVmssInstance parancsmag a megadott virtuálisgép-készlet (VMSS-példány) kézi frissítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="d5fe6-107">Ezt a beállítást akkor használja a rendszer, ha a VMSS-méretarány beállítása beállítás manuális értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="d5fe6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d5fe6-108">EXAMPLES</span></span>

### <span data-ttu-id="d5fe6-109">Példa 1: a VMSS példány frissítésének megkezdése</span><span class="sxs-lookup"><span data-stu-id="d5fe6-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="d5fe6-110">Ez a parancs elindítja a VMScaleSet001 nevű VMSS frissítését, amelynek a példány azonosítója 0.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="d5fe6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5fe6-111">PARAMETERS</span></span>

### <span data-ttu-id="d5fe6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5fe6-112">-AsJob</span></span>
<span data-ttu-id="d5fe6-113">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d5fe6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fe6-114">-DefaultProfile</span></span>
<span data-ttu-id="d5fe6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5fe6-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d5fe6-116">-InstanceId</span></span>
<span data-ttu-id="d5fe6-117">Karakterláncként adja meg a frissítendő példány AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="d5fe6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5fe6-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5fe6-119">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d5fe6-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d5fe6-120">-VMScaleSetName</span></span>
<span data-ttu-id="d5fe6-121">Annak a VMSS-példánynak a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="d5fe6-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5fe6-122">-Confirm</span></span>
<span data-ttu-id="d5fe6-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5fe6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5fe6-124">-WhatIf</span></span>
<span data-ttu-id="d5fe6-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d5fe6-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5fe6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fe6-127">CommonParameters</span></span>
<span data-ttu-id="d5fe6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5fe6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fe6-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fe6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fe6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5fe6-130">INPUTS</span></span>

### <span data-ttu-id="d5fe6-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="d5fe6-131">None</span></span>
<span data-ttu-id="d5fe6-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5fe6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5fe6-133">OUTPUTS</span></span>

###  
<span data-ttu-id="d5fe6-134">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d5fe6-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5fe6-135">NOTES</span></span>

## <span data-ttu-id="d5fe6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5fe6-136">RELATED LINKS</span></span>

[<span data-ttu-id="d5fe6-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d5fe6-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


