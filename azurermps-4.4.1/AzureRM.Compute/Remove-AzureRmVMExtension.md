---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: 164fdd36ca0e97dde33caec1322ddfa2bb6a15c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492541"
---
# <span data-ttu-id="c3ec2-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c3ec2-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="c3ec2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ec2-103">Eltávolít egy virtuális gépről a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3ec2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3ec2-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3ec2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3ec2-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ec2-106">A **Remove-AzureRmVMExtension** parancsmag eltávolítja a virtuális gép virtuálisgép-bővítményeinek bővítményét.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="c3ec2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3ec2-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ec2-108">1. példa: bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="c3ec2-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="c3ec2-109">Ez a parancs eltávolítja a ContosoTest nevű bővítményt a ResourceGroup11 nevű VirtualMachine22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="c3ec2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3ec2-110">PARAMETERS</span></span>

### <span data-ttu-id="c3ec2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ec2-111">-DefaultProfile</span></span>
<span data-ttu-id="c3ec2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ec2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c3ec2-113">-Force</span></span>
<span data-ttu-id="c3ec2-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3ec2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3ec2-115">-Name</span></span>
<span data-ttu-id="c3ec2-116">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c3ec2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ec2-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3ec2-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c3ec2-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="c3ec2-119">-VMName</span></span>
<span data-ttu-id="c3ec2-120">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="c3ec2-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3ec2-121">-Confirm</span></span>
<span data-ttu-id="c3ec2-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ec2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ec2-123">-WhatIf</span></span>
<span data-ttu-id="c3ec2-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c3ec2-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3ec2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ec2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ec2-126">CommonParameters</span></span>
<span data-ttu-id="c3ec2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3ec2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ec2-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ec2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ec2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3ec2-129">INPUTS</span></span>

## <span data-ttu-id="c3ec2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3ec2-130">OUTPUTS</span></span>

## <span data-ttu-id="c3ec2-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3ec2-131">NOTES</span></span>

## <span data-ttu-id="c3ec2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3ec2-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3ec2-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c3ec2-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="c3ec2-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c3ec2-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


