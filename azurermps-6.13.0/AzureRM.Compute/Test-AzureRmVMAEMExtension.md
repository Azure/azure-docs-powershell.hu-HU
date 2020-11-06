---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: ab4b746b19f42831b690a61e6300b3205cf7d41b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499664"
---
# <span data-ttu-id="1db3e-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1db3e-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="1db3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1db3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1db3e-103">Ellenőrzi az agrár-AEM bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1db3e-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1db3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1db3e-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1db3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1db3e-105">DESCRIPTION</span></span>
<span data-ttu-id="1db3e-106">A **teszt-AzureRmVMAEMExtension** parancsmag ellenőrzi az Azure Enhanced monitoring (AEM) bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1db3e-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="1db3e-107">Az agrár-(AEM) bővítmény összegyűjti a teljesítménnyel kapcsolatos adatokat.</span><span class="sxs-lookup"><span data-stu-id="1db3e-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="1db3e-108">Ez a parancsmag ellenőrzi, hogy elérhetők-e a teljesítményadatok.</span><span class="sxs-lookup"><span data-stu-id="1db3e-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="1db3e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1db3e-109">EXAMPLES</span></span>

### <span data-ttu-id="1db3e-110">1. példa: az AEM-bővítmény konfigurációjának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="1db3e-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="1db3e-111">Ez a parancs ellenőrzi a contoso-Server nevű virtuális gép AEM-bővítményének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1db3e-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="1db3e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1db3e-112">PARAMETERS</span></span>

### <span data-ttu-id="1db3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db3e-113">-DefaultProfile</span></span>
<span data-ttu-id="1db3e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1db3e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1db3e-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="1db3e-115">-OSType</span></span>
<span data-ttu-id="1db3e-116">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="1db3e-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="1db3e-117">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="1db3e-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="1db3e-118">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="1db3e-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="1db3e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db3e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1db3e-120">Annak a virtuális gépnek az erőforráscsoport-csoportjának a nevét adja meg, amelyre a parancsmag ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="1db3e-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="1db3e-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="1db3e-121">-SkipStorageCheck</span></span>
<span data-ttu-id="1db3e-122">Jelzi, hogy ez a parancsmag kihagyja a tárterület-konfiguráció ellenőrzését.</span><span class="sxs-lookup"><span data-stu-id="1db3e-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="1db3e-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="1db3e-123">-VMName</span></span>
<span data-ttu-id="1db3e-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1db3e-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1db3e-125">Ez a parancsmag teszteli a virtuális gép AEM bővítményét, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="1db3e-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1db3e-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="1db3e-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="1db3e-127">A tárolási konfiguráció ellenőrzésének percben megadott időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1db3e-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="1db3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db3e-128">CommonParameters</span></span>
<span data-ttu-id="1db3e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1db3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db3e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1db3e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db3e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1db3e-131">INPUTS</span></span>

### <span data-ttu-id="1db3e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1db3e-132">System.String</span></span>

## <span data-ttu-id="1db3e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1db3e-133">OUTPUTS</span></span>

### <span data-ttu-id="1db3e-134">Microsoft. Azure. commands. kiszámítás. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="1db3e-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="1db3e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1db3e-135">NOTES</span></span>

## <span data-ttu-id="1db3e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1db3e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1db3e-137">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1db3e-137">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1db3e-138">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1db3e-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1db3e-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1db3e-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


