---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186809"
---
# <span data-ttu-id="03bc2-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="03bc2-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="03bc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="03bc2-103">A VMs-rendszer merevlemez-titkosítási állapotát jeleníti meg VM-méretarányban.</span><span class="sxs-lookup"><span data-stu-id="03bc2-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="03bc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03bc2-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03bc2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="03bc2-106">A VM-készlet lemezvezérlő-titkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="03bc2-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="03bc2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="03bc2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03bc2-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="03bc2-109">A VM-példányok VMSS001 nevű, a VM-es verzióban a Group001 nevű erőforráscsoport csoportjába tartozó titkosítási állapotot jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="03bc2-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="03bc2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03bc2-110">PARAMETERS</span></span>

### <span data-ttu-id="03bc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bc2-111">-DefaultProfile</span></span>
<span data-ttu-id="03bc2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03bc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03bc2-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="03bc2-113">-ExtensionName</span></span>
<span data-ttu-id="03bc2-114">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="03bc2-114">The extension name.</span></span>
<span data-ttu-id="03bc2-115">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a Linux VMs-AzureDiskEncryptionForLinux használhatók.</span><span class="sxs-lookup"><span data-stu-id="03bc2-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="03bc2-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="03bc2-116">-InstanceId</span></span>
<span data-ttu-id="03bc2-117">A példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bc2-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="03bc2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03bc2-118">-ResourceGroupName</span></span>
<span data-ttu-id="03bc2-119">A virtuálisgép-készlethez tartozó erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="03bc2-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="03bc2-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="03bc2-120">-VMScaleSetName</span></span>
<span data-ttu-id="03bc2-121">A virtuálisgép-készlet beállítása név.</span><span class="sxs-lookup"><span data-stu-id="03bc2-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="03bc2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bc2-122">CommonParameters</span></span>
<span data-ttu-id="03bc2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03bc2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bc2-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="03bc2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bc2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03bc2-125">INPUTS</span></span>

### <span data-ttu-id="03bc2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="03bc2-126">System.String</span></span>

## <span data-ttu-id="03bc2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03bc2-127">OUTPUTS</span></span>

### <span data-ttu-id="03bc2-128">Microsoft. Azure. commands. kiszámítás. models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="03bc2-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="03bc2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03bc2-129">NOTES</span></span>

## <span data-ttu-id="03bc2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03bc2-130">RELATED LINKS</span></span>
