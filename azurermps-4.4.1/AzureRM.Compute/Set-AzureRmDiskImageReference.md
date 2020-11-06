---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: e111de4f6eb168afdd7b16d4d0ee0297d44fb149
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500092"
---
# <span data-ttu-id="b9e59-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="b9e59-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="b9e59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9e59-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e59-103">A kép hivatkozási tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="b9e59-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9e59-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9e59-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e59-106">A **set-AzureRmDiskImageReference** parancsmag a Képhivatkozás tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="b9e59-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="b9e59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9e59-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e59-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9e59-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="b9e59-109">Az első parancs létrehoz egy helyi merevlemez-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="b9e59-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b9e59-110">A Windows OS típust is beállítja.</span><span class="sxs-lookup"><span data-stu-id="b9e59-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="b9e59-111">A második parancs beállítja a képazonosítót és a 0 logikai egységet a Disk objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b9e59-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="b9e59-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="b9e59-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b9e59-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9e59-113">PARAMETERS</span></span>

### <span data-ttu-id="b9e59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e59-114">-DefaultProfile</span></span>
<span data-ttu-id="b9e59-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9e59-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9e59-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="b9e59-116">-Disk</span></span>
<span data-ttu-id="b9e59-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b9e59-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e59-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b9e59-118">-Id</span></span>
<span data-ttu-id="b9e59-119">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9e59-119">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e59-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="b9e59-120">-Lun</span></span>
<span data-ttu-id="b9e59-121">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9e59-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e59-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9e59-122">-Confirm</span></span>
<span data-ttu-id="b9e59-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9e59-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e59-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e59-124">-WhatIf</span></span>
<span data-ttu-id="b9e59-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9e59-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9e59-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9e59-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e59-127">CommonParameters</span></span>
<span data-ttu-id="b9e59-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9e59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e59-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e59-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e59-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e59-130">INPUTS</span></span>

### <span data-ttu-id="b9e59-131">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="b9e59-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="b9e59-132">System. String System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b9e59-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b9e59-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e59-133">OUTPUTS</span></span>

### <span data-ttu-id="b9e59-134">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="b9e59-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="b9e59-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9e59-135">NOTES</span></span>

## <span data-ttu-id="b9e59-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9e59-136">RELATED LINKS</span></span>

