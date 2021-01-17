---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477778"
---
# <span data-ttu-id="4bdaa-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4bdaa-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="4bdaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bdaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdaa-103">Egy VM-méretkészlet lemeztitkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4bdaa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4bdaa-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bdaa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4bdaa-105">DESCRIPTION</span></span>
<span data-ttu-id="4bdaa-106">Egy VM-méretkészlet lemeztitkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4bdaa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4bdaa-107">EXAMPLES</span></span>

### <span data-ttu-id="4bdaa-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4bdaa-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4bdaa-109">A VMSS001 nevű VM-skálakészlet lemeztitkosítási állapotát jeleníti meg, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4bdaa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bdaa-110">PARAMETERS</span></span>

### <span data-ttu-id="4bdaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdaa-111">-DefaultProfile</span></span>
<span data-ttu-id="4bdaa-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bdaa-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4bdaa-113">-ExtensionName</span></span>
<span data-ttu-id="4bdaa-114">A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-114">The extension name.</span></span>
<span data-ttu-id="4bdaa-115">Ha nincs megadva ez a paraméter, az alapértelmezett értékek a Windows-VMs és az AzureDiskEncryptionForLinux for Linux-vMs AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="4bdaa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdaa-116">-ResourceGroupName</span></span>
<span data-ttu-id="4bdaa-117">A virtuális gép méretaránykészletének erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="4bdaa-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="4bdaa-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4bdaa-118">-VMScaleSetName</span></span>
<span data-ttu-id="4bdaa-119">A virtuális gép méretaránykészletének neve.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="4bdaa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdaa-120">CommonParameters</span></span>
<span data-ttu-id="4bdaa-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdaa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdaa-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bdaa-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdaa-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bdaa-123">INPUTS</span></span>

### <span data-ttu-id="4bdaa-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4bdaa-124">System.String</span></span>

## <span data-ttu-id="4bdaa-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bdaa-125">OUTPUTS</span></span>

### <span data-ttu-id="4bdaa-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="4bdaa-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="4bdaa-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4bdaa-127">NOTES</span></span>

## <span data-ttu-id="4bdaa-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bdaa-128">RELATED LINKS</span></span>
