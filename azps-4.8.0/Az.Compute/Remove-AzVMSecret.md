---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018108"
---
# <span data-ttu-id="49102-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="49102-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="49102-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49102-102">SYNOPSIS</span></span>
<span data-ttu-id="49102-103">Titkos (a) titok eltávolítása egy virtuális gép objektumból</span><span class="sxs-lookup"><span data-stu-id="49102-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="49102-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49102-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49102-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49102-105">DESCRIPTION</span></span>
<span data-ttu-id="49102-106">A Remove-AzVMSecret parancsmag eltávolítja (a) titkos (ek) et egy virtuális Machine-objektumból.</span><span class="sxs-lookup"><span data-stu-id="49102-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="49102-107">Példák</span><span class="sxs-lookup"><span data-stu-id="49102-107">EXAMPLES</span></span>

### <span data-ttu-id="49102-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49102-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="49102-109">A virtuális gép "VM1" "rg1" erőforráscsoport minden titkát eltávolítja, és frissíti a VM-et.</span><span class="sxs-lookup"><span data-stu-id="49102-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="49102-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49102-110">PARAMETERS</span></span>

### <span data-ttu-id="49102-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49102-111">-DefaultProfile</span></span>
<span data-ttu-id="49102-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49102-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49102-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="49102-113">-SourceVaultId</span></span>
<span data-ttu-id="49102-114">A parancsmag által eltávolított forrás-tároló azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49102-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="49102-115">-VM</span><span class="sxs-lookup"><span data-stu-id="49102-115">-VM</span></span>
<span data-ttu-id="49102-116">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja (a) titkos (a) titkot (oka) t.</span><span class="sxs-lookup"><span data-stu-id="49102-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="49102-117">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="49102-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="49102-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49102-118">-Confirm</span></span>
<span data-ttu-id="49102-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49102-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49102-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49102-120">-WhatIf</span></span>
<span data-ttu-id="49102-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49102-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49102-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49102-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49102-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49102-123">CommonParameters</span></span>
<span data-ttu-id="49102-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49102-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49102-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49102-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49102-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49102-126">INPUTS</span></span>

### <span data-ttu-id="49102-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="49102-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="49102-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49102-128">OUTPUTS</span></span>

### <span data-ttu-id="49102-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="49102-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="49102-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49102-130">NOTES</span></span>

## <span data-ttu-id="49102-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49102-131">RELATED LINKS</span></span>
