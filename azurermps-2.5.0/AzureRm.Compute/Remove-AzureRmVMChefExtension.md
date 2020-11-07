---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: bc8dbd023d8730922614f749f540d182c63237a4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850053"
---
# <span data-ttu-id="034a2-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="034a2-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="034a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="034a2-102">SYNOPSIS</span></span>
<span data-ttu-id="034a2-103">Eltávolítja a séf kiterjesztését egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="034a2-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="034a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="034a2-104">SYNTAX</span></span>

### <span data-ttu-id="034a2-105">Linux</span><span class="sxs-lookup"><span data-stu-id="034a2-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="034a2-106">Windows</span><span class="sxs-lookup"><span data-stu-id="034a2-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="034a2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="034a2-107">DESCRIPTION</span></span>
<span data-ttu-id="034a2-108">A **Remove-AzureVMChefExtension** parancsmag eltávolítja a Chef bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="034a2-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="034a2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="034a2-109">EXAMPLES</span></span>

### <span data-ttu-id="034a2-110">Példa 1: Chef-kiterjesztés eltávolítása Windows Virtual Machine-ből</span><span class="sxs-lookup"><span data-stu-id="034a2-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="034a2-111">Ez a parancs eltávolítja a Chef bővítményt egy, a WindowsVM001 nevű Windows-beli virtuális gépről, amely a ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="034a2-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="034a2-112">2. példa: Chef-kiterjesztés eltávolítása egy linuxos virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="034a2-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="034a2-113">Ez a parancs eltávolítja a Chef bővítményt egy LinuxVM001 nevű, a ResourceGroup002 nevű erőforráscsoport csoportjába tartozó Linux-beli virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="034a2-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="034a2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="034a2-114">PARAMETERS</span></span>

### <span data-ttu-id="034a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034a2-115">-DefaultProfile</span></span>
<span data-ttu-id="034a2-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="034a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="034a2-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="034a2-117">-Linux</span></span>
<span data-ttu-id="034a2-118">Azt jelzi, hogy ez a parancsmag egy linuxos virtuális gépet céloz meg.</span><span class="sxs-lookup"><span data-stu-id="034a2-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034a2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="034a2-119">-Name</span></span>
<span data-ttu-id="034a2-120">Annak a séf-bővítménynek a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="034a2-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="034a2-122">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="034a2-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="034a2-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="034a2-123">-VMName</span></span>
<span data-ttu-id="034a2-124">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja eltávolítja a szakács bővítményt.</span><span class="sxs-lookup"><span data-stu-id="034a2-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="034a2-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="034a2-125">-Windows</span></span>
<span data-ttu-id="034a2-126">Jelzi, hogy ez a parancsmag a Windows Virtual Machine-t célozza meg.</span><span class="sxs-lookup"><span data-stu-id="034a2-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034a2-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="034a2-127">-Confirm</span></span>
<span data-ttu-id="034a2-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="034a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034a2-129">-WhatIf</span></span>
<span data-ttu-id="034a2-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="034a2-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="034a2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="034a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034a2-132">CommonParameters</span></span>
<span data-ttu-id="034a2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="034a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034a2-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034a2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034a2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="034a2-135">INPUTS</span></span>

### <span data-ttu-id="034a2-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="034a2-136">None</span></span>
<span data-ttu-id="034a2-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="034a2-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="034a2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="034a2-138">OUTPUTS</span></span>

### <span data-ttu-id="034a2-139">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="034a2-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="034a2-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="034a2-140">NOTES</span></span>

## <span data-ttu-id="034a2-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="034a2-141">RELATED LINKS</span></span>

[<span data-ttu-id="034a2-142">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="034a2-142">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="034a2-143">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="034a2-143">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
