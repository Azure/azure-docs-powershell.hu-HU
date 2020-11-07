---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680192"
---
# <span data-ttu-id="68b21-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="68b21-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="68b21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68b21-102">SYNOPSIS</span></span>
<span data-ttu-id="68b21-103">Információt kap az agrár-és az agrár-mellékről.</span><span class="sxs-lookup"><span data-stu-id="68b21-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68b21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68b21-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="68b21-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68b21-105">DESCRIPTION</span></span>
<span data-ttu-id="68b21-106">A **Get-AzureRmVMAEMExtension** parancsmag információkat kap az Azure Enhanced monitoring (AEM) bővítményről.</span><span class="sxs-lookup"><span data-stu-id="68b21-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="68b21-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68b21-107">EXAMPLES</span></span>

### <span data-ttu-id="68b21-108">1. példa: az AEM-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="68b21-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="68b21-109">Ez a parancs a contoso-Server nevű virtuális gép AEM-bővítményének információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="68b21-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="68b21-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68b21-110">PARAMETERS</span></span>

### <span data-ttu-id="68b21-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68b21-111">-Name</span></span>
<span data-ttu-id="68b21-112">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68b21-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="68b21-113">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="68b21-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="68b21-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="68b21-114">-OSType</span></span>
<span data-ttu-id="68b21-115">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="68b21-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="68b21-116">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="68b21-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="68b21-117">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="68b21-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="68b21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b21-118">-ResourceGroupName</span></span>
<span data-ttu-id="68b21-119">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68b21-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="68b21-120">Ez a parancsmag a virtuális gép AEM-bővítményére vonatkozó információkat kap.</span><span class="sxs-lookup"><span data-stu-id="68b21-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="68b21-121">-Állapot</span><span class="sxs-lookup"><span data-stu-id="68b21-121">-Status</span></span>
<span data-ttu-id="68b21-122">Jelzi, hogy ez a parancsmag csak az AEM bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="68b21-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="68b21-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="68b21-123">-VMName</span></span>
<span data-ttu-id="68b21-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68b21-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="68b21-125">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményéről, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="68b21-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="68b21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b21-126">CommonParameters</span></span>
<span data-ttu-id="68b21-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68b21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b21-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b21-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b21-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68b21-129">INPUTS</span></span>

### <span data-ttu-id="68b21-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="68b21-130">None</span></span>
<span data-ttu-id="68b21-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="68b21-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68b21-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68b21-132">OUTPUTS</span></span>

## <span data-ttu-id="68b21-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68b21-133">NOTES</span></span>

## <span data-ttu-id="68b21-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68b21-134">RELATED LINKS</span></span>

[<span data-ttu-id="68b21-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="68b21-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="68b21-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="68b21-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="68b21-137">Teszt-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="68b21-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


