---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 5efda3a73cc94d2e196b5817d5b3c1e507192da0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844637"
---
# <span data-ttu-id="d362e-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d362e-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="d362e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d362e-102">SYNOPSIS</span></span>
<span data-ttu-id="d362e-103">Információt kap az agrár-és az agrár-mellékről.</span><span class="sxs-lookup"><span data-stu-id="d362e-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="d362e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d362e-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d362e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d362e-105">DESCRIPTION</span></span>
<span data-ttu-id="d362e-106">A **Get-AzVMAEMExtension** parancsmag információkat kap az Azure Enhanced monitoring (AEM) bővítményről.</span><span class="sxs-lookup"><span data-stu-id="d362e-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="d362e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d362e-107">EXAMPLES</span></span>

### <span data-ttu-id="d362e-108">1. példa: az AEM-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="d362e-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="d362e-109">Ez a parancs a contoso-Server nevű virtuális gép AEM-bővítményének információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d362e-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="d362e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d362e-110">PARAMETERS</span></span>

### <span data-ttu-id="d362e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d362e-111">-DefaultProfile</span></span>
<span data-ttu-id="d362e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d362e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d362e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d362e-113">-Name</span></span>
<span data-ttu-id="d362e-114">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d362e-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d362e-115">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="d362e-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="d362e-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="d362e-116">-OSType</span></span>
<span data-ttu-id="d362e-117">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="d362e-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d362e-118">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="d362e-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d362e-119">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="d362e-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="d362e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d362e-120">-ResourceGroupName</span></span>
<span data-ttu-id="d362e-121">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d362e-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="d362e-122">Ez a parancsmag a virtuális gép AEM-bővítményére vonatkozó információkat kap.</span><span class="sxs-lookup"><span data-stu-id="d362e-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="d362e-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="d362e-123">-Status</span></span>
<span data-ttu-id="d362e-124">Jelzi, hogy ez a parancsmag csak az AEM bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d362e-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="d362e-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="d362e-125">-VMName</span></span>
<span data-ttu-id="d362e-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d362e-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d362e-127">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményéről, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d362e-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d362e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d362e-128">CommonParameters</span></span>
<span data-ttu-id="d362e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d362e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d362e-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d362e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d362e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d362e-131">INPUTS</span></span>

### <span data-ttu-id="d362e-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="d362e-132">None</span></span>
<span data-ttu-id="d362e-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d362e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d362e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d362e-134">OUTPUTS</span></span>

### <span data-ttu-id="d362e-135">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d362e-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="d362e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d362e-136">NOTES</span></span>

## <span data-ttu-id="d362e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d362e-137">RELATED LINKS</span></span>

[<span data-ttu-id="d362e-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d362e-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="d362e-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d362e-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="d362e-140">Teszt-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d362e-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


