---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: da904e6dfbf9d85319636b3bc6ff5ced5f0b2973
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844361"
---
# <span data-ttu-id="da8a1-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="da8a1-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="da8a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="da8a1-103">Titkos (a) titok eltávolítása egy virtuális gép objektumból</span><span class="sxs-lookup"><span data-stu-id="da8a1-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="da8a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da8a1-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da8a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da8a1-105">DESCRIPTION</span></span>
<span data-ttu-id="da8a1-106">A Remove-AzVMSecret parancsmag eltávolítja (a) titkos (ek) et egy virtuális Machine-objektumból.</span><span class="sxs-lookup"><span data-stu-id="da8a1-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="da8a1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da8a1-107">EXAMPLES</span></span>

### <span data-ttu-id="da8a1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da8a1-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="da8a1-109">A virtuális gép "VM1" "rg1" erőforráscsoport minden titkát eltávolítja, és frissíti a VM-et.</span><span class="sxs-lookup"><span data-stu-id="da8a1-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="da8a1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da8a1-110">PARAMETERS</span></span>

### <span data-ttu-id="da8a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8a1-111">-DefaultProfile</span></span>
<span data-ttu-id="da8a1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da8a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da8a1-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="da8a1-113">-SourceVaultId</span></span>
<span data-ttu-id="da8a1-114">A parancsmag által eltávolított forrás-tároló azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da8a1-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="da8a1-115">-VM</span><span class="sxs-lookup"><span data-stu-id="da8a1-115">-VM</span></span>
<span data-ttu-id="da8a1-116">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja (a) titkos (a) titkot (oka) t.</span><span class="sxs-lookup"><span data-stu-id="da8a1-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="da8a1-117">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="da8a1-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="da8a1-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da8a1-118">-Confirm</span></span>
<span data-ttu-id="da8a1-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da8a1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da8a1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da8a1-120">-WhatIf</span></span>
<span data-ttu-id="da8a1-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da8a1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da8a1-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da8a1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da8a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8a1-123">CommonParameters</span></span>
<span data-ttu-id="da8a1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da8a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8a1-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da8a1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8a1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da8a1-126">INPUTS</span></span>

### <span data-ttu-id="da8a1-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="da8a1-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="da8a1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da8a1-128">OUTPUTS</span></span>

### <span data-ttu-id="da8a1-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="da8a1-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="da8a1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da8a1-130">NOTES</span></span>

## <span data-ttu-id="da8a1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da8a1-131">RELATED LINKS</span></span>

