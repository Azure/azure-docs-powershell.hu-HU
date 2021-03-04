---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: ed5f79763d8e9786f0a502f404474eeef2f641f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922113"
---
# <span data-ttu-id="71503-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="71503-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="71503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71503-102">SYNOPSIS</span></span>
<span data-ttu-id="71503-103">Információkat kap az AEM bővítményről.</span><span class="sxs-lookup"><span data-stu-id="71503-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="71503-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71503-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71503-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71503-105">DESCRIPTION</span></span>
<span data-ttu-id="71503-106">A **Get-AzVMAEMExtension** parancsmag információt kap az Azure Enhanced Monitoring (AEM) bővítményről.</span><span class="sxs-lookup"><span data-stu-id="71503-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="71503-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71503-107">EXAMPLES</span></span>

### <span data-ttu-id="71503-108">1. példa: Az AEM-bővítmény lekérte</span><span class="sxs-lookup"><span data-stu-id="71503-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="71503-109">Ez a parancs információkat kap a contoso-kiszolgáló nevű virtuális gép AEM-bővítményéhez.</span><span class="sxs-lookup"><span data-stu-id="71503-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="71503-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71503-110">PARAMETERS</span></span>

### <span data-ttu-id="71503-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71503-111">-DefaultProfile</span></span>
<span data-ttu-id="71503-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71503-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71503-113">-Name</span><span class="sxs-lookup"><span data-stu-id="71503-113">-Name</span></span>
<span data-ttu-id="71503-114">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71503-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="71503-115">Ez a parancsmag információt kap az AEM bővítményről a parancsmag által megadott virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="71503-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="71503-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="71503-116">-OSType</span></span>
<span data-ttu-id="71503-117">Az operációs rendszer lemezének típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="71503-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="71503-118">Ha az operációs rendszer lemezének nincs típusa, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="71503-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="71503-119">A paraméter elfogadható értékei a következőek: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="71503-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="71503-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71503-120">-ResourceGroupName</span></span>
<span data-ttu-id="71503-121">Egy virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="71503-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="71503-122">Ez a parancsmag információt kap a virtuális gépen található AEM-bővítményről.</span><span class="sxs-lookup"><span data-stu-id="71503-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="71503-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="71503-123">-Status</span></span>
<span data-ttu-id="71503-124">Azt jelzi, hogy ez a parancsmag csak az AEM kiterjesztés példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="71503-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="71503-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="71503-125">-VMName</span></span>
<span data-ttu-id="71503-126">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71503-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="71503-127">Ez a parancsmag információt kap a paraméter által megadott virtuális gép AEM-bővítményével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="71503-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="71503-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71503-128">CommonParameters</span></span>
<span data-ttu-id="71503-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71503-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71503-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71503-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71503-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71503-131">INPUTS</span></span>

### <span data-ttu-id="71503-132">System.String</span><span class="sxs-lookup"><span data-stu-id="71503-132">System.String</span></span>

### <span data-ttu-id="71503-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71503-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71503-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71503-134">OUTPUTS</span></span>

### <span data-ttu-id="71503-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="71503-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="71503-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71503-136">NOTES</span></span>

## <span data-ttu-id="71503-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71503-137">RELATED LINKS</span></span>

[<span data-ttu-id="71503-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="71503-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="71503-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="71503-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="71503-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="71503-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


