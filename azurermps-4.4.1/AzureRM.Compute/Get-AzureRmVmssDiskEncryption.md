---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 045265a347b4a8bbcc387079f3c5a27a629a8ec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500879"
---
# <span data-ttu-id="4c7f4-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4c7f4-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="4c7f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7f4-103">A VM-léptékű készlet lemez-titkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c7f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c7f4-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c7f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="4c7f4-106">A VM-léptékű készlet lemez-titkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4c7f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4c7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="4c7f4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c7f4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4c7f4-109">A Group001 nevű erőforráscsoporthoz tartozó VMSS001 nevű VM-skála adatkészletének Disk Encryption állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4c7f4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c7f4-110">PARAMETERS</span></span>

### <span data-ttu-id="4c7f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7f4-111">-DefaultProfile</span></span>
<span data-ttu-id="4c7f4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c7f4-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4c7f4-113">-ExtensionName</span></span>
<span data-ttu-id="4c7f4-114">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-114">The extension name.</span></span>
<span data-ttu-id="4c7f4-115">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a Linux VMs-AzureDiskEncryptionForLinux használhatók.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="4c7f4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c7f4-116">-ResourceGroupName</span></span>
<span data-ttu-id="4c7f4-117">A virtuálisgép-készlethez tartozó erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4c7f4-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="4c7f4-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4c7f4-118">-VMScaleSetName</span></span>
<span data-ttu-id="4c7f4-119">A virtuálisgép-készlet beállítása név.</span><span class="sxs-lookup"><span data-stu-id="4c7f4-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="4c7f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7f4-120">CommonParameters</span></span>
<span data-ttu-id="4c7f4-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c7f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7f4-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c7f4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7f4-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c7f4-123">INPUTS</span></span>

### <span data-ttu-id="4c7f4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4c7f4-124">System.String</span></span>

## <span data-ttu-id="4c7f4-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c7f4-125">OUTPUTS</span></span>

### <span data-ttu-id="4c7f4-126">Microsoft. Azure. commands. kiszámítás. models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="4c7f4-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="4c7f4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c7f4-127">NOTES</span></span>

## <span data-ttu-id="4c7f4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c7f4-128">RELATED LINKS</span></span>

