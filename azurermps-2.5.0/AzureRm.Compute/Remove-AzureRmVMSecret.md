---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 8d3c10be9d4a3f165932271838f6af8fdbf18e4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849737"
---
# <span data-ttu-id="7f1b1-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="7f1b1-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="7f1b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1b1-103">Titkos (a) titok eltávolítása egy virtuális gép objektumból</span><span class="sxs-lookup"><span data-stu-id="7f1b1-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f1b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f1b1-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f1b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f1b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1b1-106">A Remove-AzureRmVMSecret parancsmag eltávolítja (a) titkos (ek) et egy virtuális Machine-objektumból.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="7f1b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7f1b1-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1b1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7f1b1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="7f1b1-109">A virtuális gép "VM1" "rg1" erőforráscsoport minden titkát eltávolítja, és frissíti a VM-et.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="7f1b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f1b1-110">PARAMETERS</span></span>

### <span data-ttu-id="7f1b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1b1-111">-DefaultProfile</span></span>
<span data-ttu-id="7f1b1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f1b1-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="7f1b1-113">-SourceVaultId</span></span>
<span data-ttu-id="7f1b1-114">A parancsmag által eltávolított forrás-tároló azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1b1-115">-VM</span><span class="sxs-lookup"><span data-stu-id="7f1b1-115">-VM</span></span>
<span data-ttu-id="7f1b1-116">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja (a) titkos (a) titkot (oka) t.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="7f1b1-117">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1b1-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f1b1-118">-Confirm</span></span>
<span data-ttu-id="7f1b1-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f1b1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f1b1-120">-WhatIf</span></span>
<span data-ttu-id="7f1b1-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f1b1-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f1b1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f1b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1b1-123">CommonParameters</span></span>
<span data-ttu-id="7f1b1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f1b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1b1-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f1b1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1b1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f1b1-126">INPUTS</span></span>

### <span data-ttu-id="7f1b1-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7f1b1-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7f1b1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f1b1-128">OUTPUTS</span></span>

### <span data-ttu-id="7f1b1-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7f1b1-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7f1b1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f1b1-130">NOTES</span></span>

## <span data-ttu-id="7f1b1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f1b1-131">RELATED LINKS</span></span>

