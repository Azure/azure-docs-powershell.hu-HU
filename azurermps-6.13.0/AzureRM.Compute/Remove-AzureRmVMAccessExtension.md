---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0360bcdb766de681ab6f54682007076e18266051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672119"
---
# <span data-ttu-id="3b871-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3b871-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="3b871-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b871-102">SYNOPSIS</span></span>
<span data-ttu-id="3b871-103">Eltávolítja a VMAccess-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3b871-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b871-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b871-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b871-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b871-105">DESCRIPTION</span></span>
<span data-ttu-id="3b871-106">A **Remove-AzureRmVMAccessExtension** parancsmag eltávolítja a virtuálisgép-hozzáférés (VMAccess) virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3b871-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="3b871-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b871-107">EXAMPLES</span></span>

## <span data-ttu-id="3b871-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b871-108">PARAMETERS</span></span>

### <span data-ttu-id="3b871-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b871-109">-DefaultProfile</span></span>
<span data-ttu-id="3b871-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b871-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b871-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3b871-111">-Force</span></span>
<span data-ttu-id="3b871-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3b871-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b871-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b871-113">-Name</span></span>
<span data-ttu-id="3b871-114">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3b871-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b871-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b871-115">-ResourceGroupName</span></span>
<span data-ttu-id="3b871-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b871-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3b871-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="3b871-117">-VMName</span></span>
<span data-ttu-id="3b871-118">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b871-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3b871-119">Ez a parancsmag eltávolítja a VMAccess a virtuális gép számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b871-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b871-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b871-120">-Confirm</span></span>
<span data-ttu-id="3b871-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b871-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b871-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b871-122">-WhatIf</span></span>
<span data-ttu-id="3b871-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b871-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b871-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b871-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b871-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b871-125">CommonParameters</span></span>
<span data-ttu-id="3b871-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b871-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b871-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b871-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b871-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b871-128">INPUTS</span></span>

### <span data-ttu-id="3b871-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3b871-129">System.String</span></span>

## <span data-ttu-id="3b871-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b871-130">OUTPUTS</span></span>

### <span data-ttu-id="3b871-131">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3b871-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3b871-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b871-132">NOTES</span></span>

## <span data-ttu-id="3b871-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b871-133">RELATED LINKS</span></span>

[<span data-ttu-id="3b871-134">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3b871-134">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3b871-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3b871-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3b871-136">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3b871-136">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
