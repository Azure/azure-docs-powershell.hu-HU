---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492847"
---
# <span data-ttu-id="4a1bf-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="4a1bf-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="4a1bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1bf-103">A Hyper-V VM konvertálása Azure támogatott virtuális merevlemez-fájlokba</span><span class="sxs-lookup"><span data-stu-id="4a1bf-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a1bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a1bf-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a1bf-105">DESCRIPTION</span></span>
<span data-ttu-id="4a1bf-106">A Hyper-V VM konvertálása Azure támogatott virtuális merevlemez-fájlokba</span><span class="sxs-lookup"><span data-stu-id="4a1bf-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="4a1bf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4a1bf-107">EXAMPLES</span></span>

### <span data-ttu-id="4a1bf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4a1bf-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="4a1bf-109">Konvertálja a Hyper-V VM nevű "teszt" nevet az Azure által támogatott virtuális merevlemez-fájlok az aktuális mappába.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="4a1bf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a1bf-110">PARAMETERS</span></span>

### <span data-ttu-id="4a1bf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a1bf-111">-AsJob</span></span>
<span data-ttu-id="4a1bf-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1bf-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="4a1bf-113">-ExportPath</span></span>
<span data-ttu-id="4a1bf-114">Az exportálási mappa elérési útja, amely tartalmazza a lemez fájljait.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1bf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4a1bf-115">-Force</span></span>
<span data-ttu-id="4a1bf-116">Akkor is kényszerítse az exportálást, ha a meglévő mappa megtalálható.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1bf-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="4a1bf-117">-HyperVServer</span></span>
<span data-ttu-id="4a1bf-118">A Hyper-V kiszolgáló DNS-neve a "localhost" értékkel az alapértelmezett értékként.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1bf-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="4a1bf-119">-HyperVVMName</span></span>
<span data-ttu-id="4a1bf-120">A Hyper-V név neve.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1bf-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a1bf-121">-Confirm</span></span>
<span data-ttu-id="4a1bf-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1bf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1bf-123">-WhatIf</span></span>
<span data-ttu-id="4a1bf-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a1bf-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a1bf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1bf-126">CommonParameters</span></span>
<span data-ttu-id="4a1bf-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a1bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1bf-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1bf-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a1bf-129">INPUTS</span></span>

### <span data-ttu-id="4a1bf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1bf-130">System.String</span></span>

## <span data-ttu-id="4a1bf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a1bf-131">OUTPUTS</span></span>

### <span data-ttu-id="4a1bf-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="4a1bf-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="4a1bf-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a1bf-133">NOTES</span></span>

## <span data-ttu-id="4a1bf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a1bf-134">RELATED LINKS</span></span>
