---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 8d2646c56a8ac659f5beeb6695dc2899fb2f2542
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850058"
---
# <span data-ttu-id="84333-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="84333-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="84333-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84333-102">SYNOPSIS</span></span>
<span data-ttu-id="84333-103">Eltávolítja a VMAccess-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="84333-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84333-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84333-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84333-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84333-105">DESCRIPTION</span></span>
<span data-ttu-id="84333-106">A **Remove-AzureRmVMAccessExtension** parancsmag eltávolítja a virtuálisgép-hozzáférés (VMAccess) virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="84333-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="84333-107">Példák</span><span class="sxs-lookup"><span data-stu-id="84333-107">EXAMPLES</span></span>

## <span data-ttu-id="84333-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84333-108">PARAMETERS</span></span>

### <span data-ttu-id="84333-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84333-109">-DefaultProfile</span></span>
<span data-ttu-id="84333-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84333-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84333-111">-Force</span><span class="sxs-lookup"><span data-stu-id="84333-111">-Force</span></span>
<span data-ttu-id="84333-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="84333-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="84333-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84333-113">-Name</span></span>
<span data-ttu-id="84333-114">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="84333-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84333-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84333-115">-ResourceGroupName</span></span>
<span data-ttu-id="84333-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84333-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="84333-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="84333-117">-VMName</span></span>
<span data-ttu-id="84333-118">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84333-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="84333-119">Ez a parancsmag eltávolítja a VMAccess a virtuális gép számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="84333-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84333-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="84333-120">-Confirm</span></span>
<span data-ttu-id="84333-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84333-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84333-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84333-122">-WhatIf</span></span>
<span data-ttu-id="84333-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="84333-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="84333-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84333-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84333-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84333-125">CommonParameters</span></span>
<span data-ttu-id="84333-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84333-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84333-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84333-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84333-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84333-128">INPUTS</span></span>

### <span data-ttu-id="84333-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="84333-129">None</span></span>
<span data-ttu-id="84333-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="84333-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84333-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84333-131">OUTPUTS</span></span>

### <span data-ttu-id="84333-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="84333-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="84333-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84333-133">NOTES</span></span>

## <span data-ttu-id="84333-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84333-134">RELATED LINKS</span></span>

[<span data-ttu-id="84333-135">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="84333-135">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="84333-136">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="84333-136">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="84333-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="84333-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
