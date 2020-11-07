---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: f5936a4be0170279d7416b05dc2b61fd22cfcca5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848902"
---
# <span data-ttu-id="ae8ac-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ae8ac-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="ae8ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8ac-103">Információt kap az agrár-és az agrár-mellékről.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae8ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae8ac-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae8ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="ae8ac-106">A **Get-AzureRmVMAEMExtension** parancsmag információkat kap az Azure Enhanced monitoring (AEM) bővítményről.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="ae8ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ae8ac-107">EXAMPLES</span></span>

### <span data-ttu-id="ae8ac-108">1. példa: az AEM-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="ae8ac-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ae8ac-109">Ez a parancs a contoso-Server nevű virtuális gép AEM-bővítményének információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ae8ac-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae8ac-110">PARAMETERS</span></span>

### <span data-ttu-id="ae8ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8ac-111">-DefaultProfile</span></span>
<span data-ttu-id="ae8ac-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae8ac-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae8ac-113">-Name</span></span>
<span data-ttu-id="ae8ac-114">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ae8ac-115">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8ac-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="ae8ac-116">-OSType</span></span>
<span data-ttu-id="ae8ac-117">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ae8ac-118">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ae8ac-119">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae8ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae8ac-121">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ae8ac-122">Ez a parancsmag a virtuális gép AEM-bővítményére vonatkozó információkat kap.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="ae8ac-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="ae8ac-123">-Status</span></span>
<span data-ttu-id="ae8ac-124">Jelzi, hogy ez a parancsmag csak az AEM bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8ac-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="ae8ac-125">-VMName</span></span>
<span data-ttu-id="ae8ac-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ae8ac-127">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményéről, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ae8ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8ac-128">CommonParameters</span></span>
<span data-ttu-id="ae8ac-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae8ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8ac-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae8ac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8ac-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae8ac-131">INPUTS</span></span>

### <span data-ttu-id="ae8ac-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="ae8ac-132">None</span></span>
<span data-ttu-id="ae8ac-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ae8ac-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae8ac-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae8ac-134">OUTPUTS</span></span>

### <span data-ttu-id="ae8ac-135">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ae8ac-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="ae8ac-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae8ac-136">NOTES</span></span>

## <span data-ttu-id="ae8ac-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae8ac-137">RELATED LINKS</span></span>

[<span data-ttu-id="ae8ac-138">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ae8ac-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ae8ac-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ae8ac-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ae8ac-140">Teszt-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ae8ac-140">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


