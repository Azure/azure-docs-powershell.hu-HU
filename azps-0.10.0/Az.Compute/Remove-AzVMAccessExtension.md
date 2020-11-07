---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844401"
---
# <span data-ttu-id="eccd0-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eccd0-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="eccd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eccd0-102">SYNOPSIS</span></span>
<span data-ttu-id="eccd0-103">Eltávolítja a VMAccess-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="eccd0-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="eccd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eccd0-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eccd0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eccd0-105">DESCRIPTION</span></span>
<span data-ttu-id="eccd0-106">A **Remove-AzVMAccessExtension** parancsmag eltávolítja a virtuálisgép-hozzáférés (VMAccess) virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="eccd0-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="eccd0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eccd0-107">EXAMPLES</span></span>

## <span data-ttu-id="eccd0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eccd0-108">PARAMETERS</span></span>

### <span data-ttu-id="eccd0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eccd0-109">-DefaultProfile</span></span>
<span data-ttu-id="eccd0-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eccd0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eccd0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="eccd0-111">-Force</span></span>
<span data-ttu-id="eccd0-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="eccd0-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eccd0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eccd0-113">-Name</span></span>
<span data-ttu-id="eccd0-114">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="eccd0-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eccd0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eccd0-115">-ResourceGroupName</span></span>
<span data-ttu-id="eccd0-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eccd0-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eccd0-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="eccd0-117">-VMName</span></span>
<span data-ttu-id="eccd0-118">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eccd0-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="eccd0-119">Ez a parancsmag eltávolítja a VMAccess a virtuális gép számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="eccd0-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="eccd0-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eccd0-120">-Confirm</span></span>
<span data-ttu-id="eccd0-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eccd0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eccd0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eccd0-122">-WhatIf</span></span>
<span data-ttu-id="eccd0-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eccd0-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="eccd0-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eccd0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eccd0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eccd0-125">CommonParameters</span></span>
<span data-ttu-id="eccd0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eccd0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eccd0-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eccd0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eccd0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eccd0-128">INPUTS</span></span>

### <span data-ttu-id="eccd0-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="eccd0-129">None</span></span>
<span data-ttu-id="eccd0-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="eccd0-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eccd0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eccd0-131">OUTPUTS</span></span>

### <span data-ttu-id="eccd0-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eccd0-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eccd0-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eccd0-133">NOTES</span></span>

## <span data-ttu-id="eccd0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eccd0-134">RELATED LINKS</span></span>

[<span data-ttu-id="eccd0-135">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eccd0-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="eccd0-136">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eccd0-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="eccd0-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="eccd0-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
