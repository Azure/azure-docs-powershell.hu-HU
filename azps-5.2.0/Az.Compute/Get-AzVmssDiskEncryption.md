---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342078"
---
# <span data-ttu-id="3c821-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3c821-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="3c821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c821-102">SYNOPSIS</span></span>
<span data-ttu-id="3c821-103">Egy VM-méretkészlet lemeztitkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3c821-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="3c821-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c821-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c821-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c821-105">DESCRIPTION</span></span>
<span data-ttu-id="3c821-106">Egy VM-méretkészlet lemeztitkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3c821-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="3c821-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c821-107">EXAMPLES</span></span>

### <span data-ttu-id="3c821-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3c821-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3c821-109">A VMSS001 nevű VM-skálakészlet lemeztitkosítási állapotát jeleníti meg, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="3c821-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="3c821-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c821-110">PARAMETERS</span></span>

### <span data-ttu-id="3c821-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c821-111">-DefaultProfile</span></span>
<span data-ttu-id="3c821-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c821-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c821-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="3c821-113">-ExtensionName</span></span>
<span data-ttu-id="3c821-114">A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="3c821-114">The extension name.</span></span>
<span data-ttu-id="3c821-115">Ha nincs megadva ez a paraméter, az alapértelmezett értékek a Windows-VMs és az AzureDiskEncryptionForLinux for Linux-vMs AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="3c821-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c821-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c821-116">-ResourceGroupName</span></span>
<span data-ttu-id="3c821-117">A virtuális gép méretaránykészletének erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="3c821-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c821-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3c821-118">-VMScaleSetName</span></span>
<span data-ttu-id="3c821-119">A virtuális gép méretaránykészletének neve.</span><span class="sxs-lookup"><span data-stu-id="3c821-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c821-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c821-120">CommonParameters</span></span>
<span data-ttu-id="3c821-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c821-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c821-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c821-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c821-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c821-123">INPUTS</span></span>

### <span data-ttu-id="3c821-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3c821-124">System.String</span></span>

## <span data-ttu-id="3c821-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c821-125">OUTPUTS</span></span>

### <span data-ttu-id="3c821-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="3c821-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="3c821-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c821-127">NOTES</span></span>

## <span data-ttu-id="3c821-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c821-128">RELATED LINKS</span></span>
