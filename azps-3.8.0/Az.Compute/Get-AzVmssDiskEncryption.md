---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847341"
---
# <span data-ttu-id="c05a8-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c05a8-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="c05a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c05a8-102">SYNOPSIS</span></span>
<span data-ttu-id="c05a8-103">A VM-léptékű készlet lemez-titkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c05a8-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="c05a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c05a8-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c05a8-105">DESCRIPTION</span></span>
<span data-ttu-id="c05a8-106">A VM-léptékű készlet lemez-titkosítási állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c05a8-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="c05a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c05a8-107">EXAMPLES</span></span>

### <span data-ttu-id="c05a8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c05a8-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c05a8-109">A Group001 nevű erőforráscsoporthoz tartozó VMSS001 nevű VM-skála adatkészletének Disk Encryption állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c05a8-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c05a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c05a8-110">PARAMETERS</span></span>

### <span data-ttu-id="c05a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05a8-111">-DefaultProfile</span></span>
<span data-ttu-id="c05a8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c05a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c05a8-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c05a8-113">-ExtensionName</span></span>
<span data-ttu-id="c05a8-114">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="c05a8-114">The extension name.</span></span>
<span data-ttu-id="c05a8-115">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a Linux VMs-AzureDiskEncryptionForLinux használhatók.</span><span class="sxs-lookup"><span data-stu-id="c05a8-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="c05a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="c05a8-117">A virtuálisgép-készlethez tartozó erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c05a8-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="c05a8-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c05a8-118">-VMScaleSetName</span></span>
<span data-ttu-id="c05a8-119">A virtuálisgép-készlet beállítása név.</span><span class="sxs-lookup"><span data-stu-id="c05a8-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="c05a8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05a8-120">CommonParameters</span></span>
<span data-ttu-id="c05a8-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c05a8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05a8-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c05a8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05a8-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05a8-123">INPUTS</span></span>

### <span data-ttu-id="c05a8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c05a8-124">System.String</span></span>

## <span data-ttu-id="c05a8-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05a8-125">OUTPUTS</span></span>

### <span data-ttu-id="c05a8-126">Microsoft. Azure. commands. kiszámítás. models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="c05a8-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="c05a8-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c05a8-127">NOTES</span></span>

## <span data-ttu-id="c05a8-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c05a8-128">RELATED LINKS</span></span>