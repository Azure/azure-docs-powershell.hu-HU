---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: e1b400f2fe3ff973c586fbde9f4003732ad8c6cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844365"
---
# <span data-ttu-id="ceea6-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ceea6-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="ceea6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ceea6-102">SYNOPSIS</span></span>
<span data-ttu-id="ceea6-103">Eltávolít egy virtuális gépről a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="ceea6-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="ceea6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ceea6-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceea6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ceea6-105">DESCRIPTION</span></span>
<span data-ttu-id="ceea6-106">A **Remove-AzVMExtension** parancsmag eltávolítja a virtuális gép virtuálisgép-bővítményeinek bővítményét.</span><span class="sxs-lookup"><span data-stu-id="ceea6-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="ceea6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ceea6-107">EXAMPLES</span></span>

### <span data-ttu-id="ceea6-108">1. példa: bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="ceea6-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="ceea6-109">Ez a parancs eltávolítja a ContosoTest nevű bővítményt a ResourceGroup11 nevű VirtualMachine22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ceea6-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="ceea6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ceea6-110">PARAMETERS</span></span>

### <span data-ttu-id="ceea6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceea6-111">-DefaultProfile</span></span>
<span data-ttu-id="ceea6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ceea6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceea6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ceea6-113">-Force</span></span>
<span data-ttu-id="ceea6-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ceea6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ceea6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ceea6-115">-Name</span></span>
<span data-ttu-id="ceea6-116">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ceea6-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ceea6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceea6-117">-ResourceGroupName</span></span>
<span data-ttu-id="ceea6-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceea6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ceea6-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="ceea6-119">-VMName</span></span>
<span data-ttu-id="ceea6-120">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="ceea6-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="ceea6-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ceea6-121">-Confirm</span></span>
<span data-ttu-id="ceea6-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ceea6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceea6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceea6-123">-WhatIf</span></span>
<span data-ttu-id="ceea6-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ceea6-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ceea6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ceea6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceea6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceea6-126">CommonParameters</span></span>
<span data-ttu-id="ceea6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ceea6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceea6-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceea6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceea6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceea6-129">INPUTS</span></span>

### <span data-ttu-id="ceea6-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="ceea6-130">None</span></span>
<span data-ttu-id="ceea6-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ceea6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ceea6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceea6-132">OUTPUTS</span></span>

### <span data-ttu-id="ceea6-133">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ceea6-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ceea6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ceea6-134">NOTES</span></span>

## <span data-ttu-id="ceea6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceea6-135">RELATED LINKS</span></span>

[<span data-ttu-id="ceea6-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ceea6-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="ceea6-137">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ceea6-137">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


