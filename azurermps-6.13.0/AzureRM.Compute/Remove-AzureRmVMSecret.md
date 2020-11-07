---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 3b7aebf0f0387de728d04ee83fdbce8ee108e207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679607"
---
# <span data-ttu-id="6a5d7-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="6a5d7-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="6a5d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5d7-103">Titkos (a) titok eltávolítása egy virtuális gép objektumból</span><span class="sxs-lookup"><span data-stu-id="6a5d7-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a5d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a5d7-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a5d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="6a5d7-106">A Remove-AzureRmVMSecret parancsmag eltávolítja (a) titkos (ek) et egy virtuális Machine-objektumból.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="6a5d7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a5d7-107">EXAMPLES</span></span>

### <span data-ttu-id="6a5d7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a5d7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="6a5d7-109">A virtuális gép "VM1" "rg1" erőforráscsoport minden titkát eltávolítja, és frissíti a VM-et.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="6a5d7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a5d7-110">PARAMETERS</span></span>

### <span data-ttu-id="6a5d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5d7-111">-DefaultProfile</span></span>
<span data-ttu-id="6a5d7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a5d7-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6a5d7-113">-SourceVaultId</span></span>
<span data-ttu-id="6a5d7-114">A parancsmag által eltávolított forrás-tároló azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a5d7-115">-VM</span><span class="sxs-lookup"><span data-stu-id="6a5d7-115">-VM</span></span>
<span data-ttu-id="6a5d7-116">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja (a) titkos (a) titkot (oka) t.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="6a5d7-117">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="6a5d7-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a5d7-118">-Confirm</span></span>
<span data-ttu-id="6a5d7-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a5d7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a5d7-120">-WhatIf</span></span>
<span data-ttu-id="6a5d7-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a5d7-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a5d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5d7-123">CommonParameters</span></span>
<span data-ttu-id="6a5d7-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a5d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5d7-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a5d7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5d7-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a5d7-126">INPUTS</span></span>

### <span data-ttu-id="6a5d7-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a5d7-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6a5d7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a5d7-128">OUTPUTS</span></span>

### <span data-ttu-id="6a5d7-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a5d7-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6a5d7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a5d7-130">NOTES</span></span>

## <span data-ttu-id="6a5d7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a5d7-131">RELATED LINKS</span></span>
