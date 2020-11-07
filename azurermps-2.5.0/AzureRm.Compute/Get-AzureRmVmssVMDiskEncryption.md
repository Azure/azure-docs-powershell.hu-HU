---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
ms.openlocfilehash: 41c18a3f9b1536e837ab8e127bfe00b62c74b5e1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850461"
---
# <span data-ttu-id="f23ba-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f23ba-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="f23ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f23ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f23ba-103">A VMs-rendszer merevlemez-titkosítási állapotát jeleníti meg VM-méretarányban.</span><span class="sxs-lookup"><span data-stu-id="f23ba-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f23ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f23ba-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f23ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f23ba-105">DESCRIPTION</span></span>
<span data-ttu-id="f23ba-106">A VM-készlet lemezvezérlő-titkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f23ba-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="f23ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f23ba-107">EXAMPLES</span></span>

### <span data-ttu-id="f23ba-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f23ba-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="f23ba-109">A VM-példányok VMSS001 nevű, a VM-es verzióban a Group001 nevű erőforráscsoport csoportjába tartozó titkosítási állapotot jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f23ba-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f23ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f23ba-110">PARAMETERS</span></span>

### <span data-ttu-id="f23ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23ba-111">-DefaultProfile</span></span>
<span data-ttu-id="f23ba-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f23ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f23ba-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f23ba-113">-ExtensionName</span></span>
<span data-ttu-id="f23ba-114">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="f23ba-114">The extension name.</span></span>
<span data-ttu-id="f23ba-115">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a Linux VMs-AzureDiskEncryptionForLinux használhatók.</span><span class="sxs-lookup"><span data-stu-id="f23ba-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="f23ba-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f23ba-116">-InstanceId</span></span>
<span data-ttu-id="f23ba-117">A példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f23ba-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="f23ba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23ba-118">-ResourceGroupName</span></span>
<span data-ttu-id="f23ba-119">A virtuálisgép-készlethez tartozó erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f23ba-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f23ba-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f23ba-120">-VMScaleSetName</span></span>
<span data-ttu-id="f23ba-121">A virtuálisgép-készlet beállítása név.</span><span class="sxs-lookup"><span data-stu-id="f23ba-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="f23ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23ba-122">CommonParameters</span></span>
<span data-ttu-id="f23ba-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f23ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23ba-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23ba-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23ba-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f23ba-125">INPUTS</span></span>

### <span data-ttu-id="f23ba-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f23ba-126">System.String</span></span>

## <span data-ttu-id="f23ba-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f23ba-127">OUTPUTS</span></span>

### <span data-ttu-id="f23ba-128">Microsoft. Azure. commands. kiszámítás. models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="f23ba-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="f23ba-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f23ba-129">NOTES</span></span>

## <span data-ttu-id="f23ba-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f23ba-130">RELATED LINKS</span></span>

