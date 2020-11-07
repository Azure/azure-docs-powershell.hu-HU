---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 25bf6699887219cb4315465d7e0f709f82849438
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844297"
---
# <span data-ttu-id="1b490-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="1b490-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="1b490-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b490-102">SYNOPSIS</span></span>
<span data-ttu-id="1b490-103">A kép hivatkozási tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="1b490-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="1b490-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b490-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b490-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b490-105">DESCRIPTION</span></span>
<span data-ttu-id="1b490-106">A **set-AzDiskImageReference** parancsmag a Képhivatkozás tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="1b490-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="1b490-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1b490-107">EXAMPLES</span></span>

### <span data-ttu-id="1b490-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1b490-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="1b490-109">Az első parancs létrehoz egy helyi merevlemez-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="1b490-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="1b490-110">A Windows OS típust is beállítja.</span><span class="sxs-lookup"><span data-stu-id="1b490-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="1b490-111">A második parancs beállítja a képazonosítót és a 0 logikai egység számát a obejct.</span><span class="sxs-lookup"><span data-stu-id="1b490-111">The second command sets the image id and the logical unit number 0 for the disk obejct.</span></span>
<span data-ttu-id="1b490-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="1b490-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1b490-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b490-113">PARAMETERS</span></span>

### <span data-ttu-id="1b490-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b490-114">-DefaultProfile</span></span>
<span data-ttu-id="1b490-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b490-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b490-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="1b490-116">-Disk</span></span>
<span data-ttu-id="1b490-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1b490-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b490-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="1b490-118">-Id</span></span>
<span data-ttu-id="1b490-119">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b490-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b490-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="1b490-120">-Lun</span></span>
<span data-ttu-id="1b490-121">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b490-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b490-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b490-122">-Confirm</span></span>
<span data-ttu-id="1b490-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b490-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b490-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b490-124">-WhatIf</span></span>
<span data-ttu-id="1b490-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b490-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b490-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b490-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b490-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b490-127">CommonParameters</span></span>
<span data-ttu-id="1b490-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b490-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b490-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b490-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b490-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b490-130">INPUTS</span></span>

### <span data-ttu-id="1b490-131">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="1b490-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="1b490-132">System. String System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1b490-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1b490-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b490-133">OUTPUTS</span></span>

### <span data-ttu-id="1b490-134">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="1b490-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="1b490-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b490-135">NOTES</span></span>

## <span data-ttu-id="1b490-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b490-136">RELATED LINKS</span></span>

