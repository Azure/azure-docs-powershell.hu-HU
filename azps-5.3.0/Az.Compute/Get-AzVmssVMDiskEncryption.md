---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477765"
---
# <span data-ttu-id="5bced-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5bced-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="5bced-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bced-102">SYNOPSIS</span></span>
<span data-ttu-id="5bced-103">A virtuális gép mérethalmazában lévő virtuális gépek lemeztitkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="5bced-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="5bced-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bced-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bced-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bced-105">DESCRIPTION</span></span>
<span data-ttu-id="5bced-106">A virtuális gép mérethalmazának lemeztitkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="5bced-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="5bced-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bced-107">EXAMPLES</span></span>

### <span data-ttu-id="5bced-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5bced-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="5bced-109">Az 1. VM-példány lemeztitkosítási állapotát jeleníti meg a VMSS001 nevű VMSS001 méretkészletben, amely a Group001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="5bced-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5bced-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bced-110">PARAMETERS</span></span>

### <span data-ttu-id="5bced-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bced-111">-DefaultProfile</span></span>
<span data-ttu-id="5bced-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bced-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bced-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5bced-113">-ExtensionName</span></span>
<span data-ttu-id="5bced-114">A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="5bced-114">The extension name.</span></span>
<span data-ttu-id="5bced-115">Ha nincs megadva ez a paraméter, az alapértelmezett értékek a Windows-VMs és az AzureDiskEncryptionForLinux for Linux-vMs AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="5bced-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5bced-116">-InstanceId</span></span>
<span data-ttu-id="5bced-117">A példányazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bced-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="5bced-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bced-118">-ResourceGroupName</span></span>
<span data-ttu-id="5bced-119">A virtuális gép méretaránykészletének erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="5bced-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5bced-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5bced-120">-VMScaleSetName</span></span>
<span data-ttu-id="5bced-121">A virtuális gép méretaránykészletének neve.</span><span class="sxs-lookup"><span data-stu-id="5bced-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bced-122">CommonParameters</span></span>
<span data-ttu-id="5bced-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bced-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bced-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bced-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bced-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bced-125">INPUTS</span></span>

### <span data-ttu-id="5bced-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5bced-126">System.String</span></span>

## <span data-ttu-id="5bced-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bced-127">OUTPUTS</span></span>

### <span data-ttu-id="5bced-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="5bced-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="5bced-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bced-129">NOTES</span></span>

## <span data-ttu-id="5bced-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bced-130">RELATED LINKS</span></span>
