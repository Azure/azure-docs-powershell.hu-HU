---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 97ddf35b453b324cf04309afd3a90be185d43224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679102"
---
# <span data-ttu-id="db45d-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="db45d-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="db45d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db45d-102">SYNOPSIS</span></span>
<span data-ttu-id="db45d-103">Eltávolítja a VMAccess-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="db45d-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db45d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db45d-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db45d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db45d-105">DESCRIPTION</span></span>
<span data-ttu-id="db45d-106">A **Remove-AzureRmVMAccessExtension** parancsmag eltávolítja a virtuálisgép-hozzáférés (VMAccess) virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="db45d-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="db45d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db45d-107">EXAMPLES</span></span>

## <span data-ttu-id="db45d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db45d-108">PARAMETERS</span></span>

### <span data-ttu-id="db45d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db45d-109">-DefaultProfile</span></span>
<span data-ttu-id="db45d-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db45d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db45d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="db45d-111">-Force</span></span>
<span data-ttu-id="db45d-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="db45d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db45d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db45d-113">-Name</span></span>
<span data-ttu-id="db45d-114">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="db45d-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="db45d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db45d-115">-ResourceGroupName</span></span>
<span data-ttu-id="db45d-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db45d-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="db45d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="db45d-117">-VMName</span></span>
<span data-ttu-id="db45d-118">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db45d-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="db45d-119">Ez a parancsmag eltávolítja a VMAccess a virtuális gép számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="db45d-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="db45d-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db45d-120">-Confirm</span></span>
<span data-ttu-id="db45d-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db45d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db45d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db45d-122">-WhatIf</span></span>
<span data-ttu-id="db45d-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db45d-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="db45d-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db45d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db45d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db45d-125">CommonParameters</span></span>
<span data-ttu-id="db45d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db45d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db45d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db45d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db45d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db45d-128">INPUTS</span></span>

## <span data-ttu-id="db45d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db45d-129">OUTPUTS</span></span>

## <span data-ttu-id="db45d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db45d-130">NOTES</span></span>

## <span data-ttu-id="db45d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db45d-131">RELATED LINKS</span></span>

[<span data-ttu-id="db45d-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="db45d-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="db45d-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="db45d-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="db45d-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="db45d-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
