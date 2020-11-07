---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 9f9b8f28fd3b2597dede1b9fe50780b2c5e43abb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671275"
---
# <span data-ttu-id="91428-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="91428-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="91428-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91428-102">SYNOPSIS</span></span>
<span data-ttu-id="91428-103">Titkos (a) titok eltávolítása egy virtuális gép objektumból</span><span class="sxs-lookup"><span data-stu-id="91428-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="91428-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91428-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91428-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91428-105">DESCRIPTION</span></span>
<span data-ttu-id="91428-106">A Remove-AzVMSecret parancsmag eltávolítja (a) titkos (ek) et egy virtuális Machine-objektumból.</span><span class="sxs-lookup"><span data-stu-id="91428-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="91428-107">Példák</span><span class="sxs-lookup"><span data-stu-id="91428-107">EXAMPLES</span></span>

### <span data-ttu-id="91428-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91428-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="91428-109">A virtuális gép "VM1" "rg1" erőforráscsoport minden titkát eltávolítja, és frissíti a VM-et.</span><span class="sxs-lookup"><span data-stu-id="91428-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="91428-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91428-110">PARAMETERS</span></span>

### <span data-ttu-id="91428-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91428-111">-DefaultProfile</span></span>
<span data-ttu-id="91428-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91428-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91428-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="91428-113">-SourceVaultId</span></span>
<span data-ttu-id="91428-114">A parancsmag által eltávolított forrás-tároló azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91428-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91428-115">-VM</span><span class="sxs-lookup"><span data-stu-id="91428-115">-VM</span></span>
<span data-ttu-id="91428-116">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja (a) titkos (a) titkot (oka) t.</span><span class="sxs-lookup"><span data-stu-id="91428-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="91428-117">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="91428-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91428-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91428-118">-Confirm</span></span>
<span data-ttu-id="91428-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91428-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91428-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91428-120">-WhatIf</span></span>
<span data-ttu-id="91428-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91428-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91428-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91428-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91428-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91428-123">CommonParameters</span></span>
<span data-ttu-id="91428-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91428-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91428-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91428-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91428-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91428-126">INPUTS</span></span>

### <span data-ttu-id="91428-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="91428-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="91428-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91428-128">OUTPUTS</span></span>

### <span data-ttu-id="91428-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="91428-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="91428-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91428-130">NOTES</span></span>

## <span data-ttu-id="91428-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91428-131">RELATED LINKS</span></span>
