---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: ae4a6d72fcb44406773234b6de55cec7ccef8eb9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850886"
---
# <span data-ttu-id="5dbb1-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dbb1-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="5dbb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5dbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbb1-103">Ellenőrzi az agrár-AEM bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dbb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5dbb1-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dbb1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5dbb1-105">DESCRIPTION</span></span>
<span data-ttu-id="5dbb1-106">A **teszt-AzureRmVMAEMExtension** parancsmag ellenőrzi az Azure Enhanced monitoring (AEM) bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="5dbb1-107">Az agrár-(AEM) bővítmény összegyűjti a teljesítménnyel kapcsolatos adatokat.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="5dbb1-108">Ez a parancsmag ellenőrzi, hogy elérhetők-e a teljesítményadatok.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="5dbb1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5dbb1-109">EXAMPLES</span></span>

### <span data-ttu-id="5dbb1-110">1. példa: az AEM-bővítmény konfigurációjának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="5dbb1-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="5dbb1-111">Ez a parancs ellenőrzi a contoso-Server nevű virtuális gép AEM-bővítményének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="5dbb1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5dbb1-112">PARAMETERS</span></span>

### <span data-ttu-id="5dbb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbb1-113">-DefaultProfile</span></span>
<span data-ttu-id="5dbb1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dbb1-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="5dbb1-115">-OSType</span></span>
<span data-ttu-id="5dbb1-116">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="5dbb1-117">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="5dbb1-118">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbb1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dbb1-119">-ResourceGroupName</span></span>
<span data-ttu-id="5dbb1-120">Annak a virtuális gépnek az erőforráscsoport-csoportjának a nevét adja meg, amelyre a parancsmag ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="5dbb1-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="5dbb1-121">-SkipStorageCheck</span></span>
<span data-ttu-id="5dbb1-122">Jelzi, hogy ez a parancsmag kihagyja a tárterület-konfiguráció ellenőrzését.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbb1-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="5dbb1-123">-VMName</span></span>
<span data-ttu-id="5dbb1-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5dbb1-125">Ez a parancsmag teszteli a virtuális gép AEM bővítményét, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbb1-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="5dbb1-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="5dbb1-127">A tárolási konfiguráció ellenőrzésének percben megadott időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbb1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbb1-128">CommonParameters</span></span>
<span data-ttu-id="5dbb1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5dbb1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbb1-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dbb1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbb1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dbb1-131">INPUTS</span></span>

### <span data-ttu-id="5dbb1-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="5dbb1-132">None</span></span>
<span data-ttu-id="5dbb1-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5dbb1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dbb1-134">OUTPUTS</span></span>

### <span data-ttu-id="5dbb1-135">Microsoft. Azure. commands. kiszámítás. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="5dbb1-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="5dbb1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5dbb1-136">NOTES</span></span>

## <span data-ttu-id="5dbb1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5dbb1-137">RELATED LINKS</span></span>

[<span data-ttu-id="5dbb1-138">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dbb1-138">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="5dbb1-139">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dbb1-139">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="5dbb1-140">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dbb1-140">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


