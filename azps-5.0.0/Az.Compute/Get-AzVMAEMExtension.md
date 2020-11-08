---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 0879458284c7e08b2e8371b9b8d8b894a482a9df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186810"
---
# <span data-ttu-id="e963b-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e963b-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="e963b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e963b-102">SYNOPSIS</span></span>
<span data-ttu-id="e963b-103">Információt kap az agrár-és az agrár-mellékről.</span><span class="sxs-lookup"><span data-stu-id="e963b-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="e963b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e963b-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e963b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e963b-105">DESCRIPTION</span></span>
<span data-ttu-id="e963b-106">A **Get-AzVMAEMExtension** parancsmag információkat kap az Azure Enhanced monitoring (AEM) bővítményről.</span><span class="sxs-lookup"><span data-stu-id="e963b-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="e963b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e963b-107">EXAMPLES</span></span>

### <span data-ttu-id="e963b-108">1. példa: az AEM-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="e963b-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="e963b-109">Ez a parancs a contoso-Server nevű virtuális gép AEM-bővítményének információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e963b-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="e963b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e963b-110">PARAMETERS</span></span>

### <span data-ttu-id="e963b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e963b-111">-DefaultProfile</span></span>
<span data-ttu-id="e963b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e963b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e963b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e963b-113">-Name</span></span>
<span data-ttu-id="e963b-114">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e963b-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e963b-115">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményére vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="e963b-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e963b-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="e963b-116">-OSType</span></span>
<span data-ttu-id="e963b-117">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="e963b-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="e963b-118">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="e963b-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="e963b-119">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="e963b-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e963b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e963b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e963b-121">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e963b-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="e963b-122">Ez a parancsmag a virtuális gép AEM-bővítményére vonatkozó információkat kap.</span><span class="sxs-lookup"><span data-stu-id="e963b-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="e963b-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="e963b-123">-Status</span></span>
<span data-ttu-id="e963b-124">Jelzi, hogy ez a parancsmag csak az AEM bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e963b-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e963b-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="e963b-125">-VMName</span></span>
<span data-ttu-id="e963b-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e963b-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e963b-127">Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményéről, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="e963b-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e963b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e963b-128">CommonParameters</span></span>
<span data-ttu-id="e963b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e963b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e963b-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e963b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e963b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e963b-131">INPUTS</span></span>

### <span data-ttu-id="e963b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e963b-132">System.String</span></span>

### <span data-ttu-id="e963b-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e963b-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e963b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e963b-134">OUTPUTS</span></span>

### <span data-ttu-id="e963b-135">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="e963b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="e963b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e963b-136">NOTES</span></span>

## <span data-ttu-id="e963b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e963b-137">RELATED LINKS</span></span>

[<span data-ttu-id="e963b-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e963b-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="e963b-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e963b-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="e963b-140">Teszt-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e963b-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


