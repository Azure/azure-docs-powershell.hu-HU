---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 040e7e557934fc90e5609a42c2e553ccf34d2f8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010774"
---
# <span data-ttu-id="4723d-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4723d-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="4723d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4723d-102">SYNOPSIS</span></span>
<span data-ttu-id="4723d-103">Ellenőrzi az AEM-bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4723d-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="4723d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4723d-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4723d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4723d-105">DESCRIPTION</span></span>
<span data-ttu-id="4723d-106">A **Test-AzVMAEMExtension** parancsmag ellenőrzi az Azure Enhanced Monitoring (AEM) bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4723d-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="4723d-107">Az AEM-bővítmény összegyűjti a teljesítményadatokat.</span><span class="sxs-lookup"><span data-stu-id="4723d-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="4723d-108">Ez a parancsmag ellenőrzi, hogy rendelkezésre állnak-e teljesítményadatok.</span><span class="sxs-lookup"><span data-stu-id="4723d-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="4723d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4723d-109">EXAMPLES</span></span>

### <span data-ttu-id="4723d-110">1. példa: Az AEM-bővítmény konfigurációjának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="4723d-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="4723d-111">Ez a parancs ellenőrzi a contoso-kiszolgáló nevű virtuális gép AEM-bővítményének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4723d-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="4723d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4723d-112">PARAMETERS</span></span>

### <span data-ttu-id="4723d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4723d-113">-DefaultProfile</span></span>
<span data-ttu-id="4723d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4723d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4723d-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="4723d-115">-OSType</span></span>
<span data-ttu-id="4723d-116">Az operációs rendszer lemezének típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4723d-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="4723d-117">Ha az operációs rendszer lemezének nincs típusa, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="4723d-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="4723d-118">A paraméter elfogadható értékei a következőek: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="4723d-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4723d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4723d-119">-ResourceGroupName</span></span>
<span data-ttu-id="4723d-120">A parancsmag által ellenőrizt virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4723d-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="4723d-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="4723d-121">-SkipStorageCheck</span></span>
<span data-ttu-id="4723d-122">Azt jelzi, hogy ez a parancsmag kihagyja a tárterület-konfiguráció ellenőrzését.</span><span class="sxs-lookup"><span data-stu-id="4723d-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4723d-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="4723d-123">-VMName</span></span>
<span data-ttu-id="4723d-124">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4723d-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4723d-125">Ez a parancsmag annak a virtuális gépnek az AEM-bővítményét teszteli, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4723d-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4723d-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="4723d-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="4723d-127">A tárterület-konfiguráció ellenőrzésének időkorrelációs idejét adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="4723d-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4723d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4723d-128">CommonParameters</span></span>
<span data-ttu-id="4723d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4723d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4723d-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4723d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4723d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4723d-131">INPUTS</span></span>

### <span data-ttu-id="4723d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4723d-132">System.String</span></span>

## <span data-ttu-id="4723d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4723d-133">OUTPUTS</span></span>

### <span data-ttu-id="4723d-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="4723d-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="4723d-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4723d-135">NOTES</span></span>

## <span data-ttu-id="4723d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4723d-136">RELATED LINKS</span></span>

[<span data-ttu-id="4723d-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4723d-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="4723d-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4723d-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="4723d-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4723d-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


