---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
ms.openlocfilehash: c45574272d814ea899e7d291b729b6a8e6526da6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493195"
---
# <span data-ttu-id="fcf73-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fcf73-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="fcf73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcf73-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf73-103">A VMs-rendszer merevlemez-titkosítási állapotát jeleníti meg VM-méretarányban.</span><span class="sxs-lookup"><span data-stu-id="fcf73-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcf73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcf73-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcf73-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcf73-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf73-106">A VM-készlet lemezvezérlő-titkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="fcf73-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="fcf73-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fcf73-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf73-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fcf73-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="fcf73-109">A VM-példányok VMSS001 nevű, a VM-es verzióban a Group001 nevű erőforráscsoport csoportjába tartozó titkosítási állapotot jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="fcf73-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="fcf73-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcf73-110">PARAMETERS</span></span>

### <span data-ttu-id="fcf73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf73-111">-DefaultProfile</span></span>
<span data-ttu-id="fcf73-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcf73-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcf73-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="fcf73-113">-ExtensionName</span></span>
<span data-ttu-id="fcf73-114">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="fcf73-114">The extension name.</span></span>
<span data-ttu-id="fcf73-115">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a Linux VMs-AzureDiskEncryptionForLinux használhatók.</span><span class="sxs-lookup"><span data-stu-id="fcf73-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf73-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fcf73-116">-InstanceId</span></span>
<span data-ttu-id="fcf73-117">A példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcf73-117">Specifies the instance ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf73-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf73-118">-ResourceGroupName</span></span>
<span data-ttu-id="fcf73-119">A virtuálisgép-készlethez tartozó erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fcf73-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="fcf73-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fcf73-120">-VMScaleSetName</span></span>
<span data-ttu-id="fcf73-121">A virtuálisgép-készlet beállítása név.</span><span class="sxs-lookup"><span data-stu-id="fcf73-121">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf73-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf73-122">CommonParameters</span></span>
<span data-ttu-id="fcf73-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcf73-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf73-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf73-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf73-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcf73-125">INPUTS</span></span>

### <span data-ttu-id="fcf73-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fcf73-126">System.String</span></span>

## <span data-ttu-id="fcf73-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcf73-127">OUTPUTS</span></span>

### <span data-ttu-id="fcf73-128">Microsoft. Azure. commands. kiszámítás. models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="fcf73-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="fcf73-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcf73-129">NOTES</span></span>

## <span data-ttu-id="fcf73-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcf73-130">RELATED LINKS</span></span>
