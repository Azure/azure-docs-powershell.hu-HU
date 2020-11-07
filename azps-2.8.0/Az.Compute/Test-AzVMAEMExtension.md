---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 7fe1219e9124a63784f3d064ffb25ed9d8271356
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667172"
---
# <span data-ttu-id="c82d8-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c82d8-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="c82d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c82d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c82d8-103">Ellenőrzi az agrár-AEM bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c82d8-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="c82d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c82d8-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c82d8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c82d8-105">DESCRIPTION</span></span>
<span data-ttu-id="c82d8-106">A **teszt-AzVMAEMExtension** parancsmag ellenőrzi az Azure Enhanced monitoring (AEM) bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c82d8-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="c82d8-107">Az agrár-(AEM) bővítmény összegyűjti a teljesítménnyel kapcsolatos adatokat.</span><span class="sxs-lookup"><span data-stu-id="c82d8-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="c82d8-108">Ez a parancsmag ellenőrzi, hogy elérhetők-e a teljesítményadatok.</span><span class="sxs-lookup"><span data-stu-id="c82d8-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="c82d8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c82d8-109">EXAMPLES</span></span>

### <span data-ttu-id="c82d8-110">1. példa: az AEM-bővítmény konfigurációjának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="c82d8-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="c82d8-111">Ez a parancs ellenőrzi a contoso-Server nevű virtuális gép AEM-bővítményének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c82d8-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="c82d8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c82d8-112">PARAMETERS</span></span>

### <span data-ttu-id="c82d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c82d8-113">-DefaultProfile</span></span>
<span data-ttu-id="c82d8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c82d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c82d8-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="c82d8-115">-OSType</span></span>
<span data-ttu-id="c82d8-116">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="c82d8-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c82d8-117">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="c82d8-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c82d8-118">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="c82d8-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="c82d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c82d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="c82d8-120">Annak a virtuális gépnek az erőforráscsoport-csoportjának a nevét adja meg, amelyre a parancsmag ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="c82d8-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="c82d8-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="c82d8-121">-SkipStorageCheck</span></span>
<span data-ttu-id="c82d8-122">Jelzi, hogy ez a parancsmag kihagyja a tárterület-konfiguráció ellenőrzését.</span><span class="sxs-lookup"><span data-stu-id="c82d8-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="c82d8-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="c82d8-123">-VMName</span></span>
<span data-ttu-id="c82d8-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c82d8-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c82d8-125">Ez a parancsmag teszteli a virtuális gép AEM bővítményét, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c82d8-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c82d8-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="c82d8-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="c82d8-127">A tárolási konfiguráció ellenőrzésének percben megadott időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c82d8-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="c82d8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82d8-128">CommonParameters</span></span>
<span data-ttu-id="c82d8-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c82d8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82d8-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c82d8-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82d8-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c82d8-131">INPUTS</span></span>

### <span data-ttu-id="c82d8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c82d8-132">System.String</span></span>

## <span data-ttu-id="c82d8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c82d8-133">OUTPUTS</span></span>

### <span data-ttu-id="c82d8-134">Microsoft. Azure. commands. kiszámítás. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="c82d8-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="c82d8-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c82d8-135">NOTES</span></span>

## <span data-ttu-id="c82d8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c82d8-136">RELATED LINKS</span></span>

[<span data-ttu-id="c82d8-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c82d8-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="c82d8-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c82d8-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="c82d8-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c82d8-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


