---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 94e5a1087f870f8dbbe099962e69d83b64f52ed3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836790"
---
# <span data-ttu-id="84149-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="84149-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="84149-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84149-102">SYNOPSIS</span></span>
<span data-ttu-id="84149-103">Rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="84149-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="84149-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84149-104">SYNTAX</span></span>

### <span data-ttu-id="84149-105">WindowsParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84149-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84149-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="84149-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84149-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="84149-107">DESCRIPTION</span></span>
<span data-ttu-id="84149-108">A **Get-AzVMBootDiagnosticsData** parancsmag rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="84149-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="84149-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84149-109">EXAMPLES</span></span>

### <span data-ttu-id="84149-110">1. példa: a rendszerindítási diagnosztika adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="84149-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="84149-111">Ez a parancs a ContosoVM07 nevű virtuális gép rendszerindítási diagnosztikai értékeit kapja.</span><span class="sxs-lookup"><span data-stu-id="84149-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="84149-112">Ez a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="84149-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="84149-113">A parancs a megadott helyi elérési utakban tárolja az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="84149-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="84149-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84149-114">PARAMETERS</span></span>

### <span data-ttu-id="84149-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84149-115">-DefaultProfile</span></span>
<span data-ttu-id="84149-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84149-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84149-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="84149-117">-Linux</span></span>
<span data-ttu-id="84149-118">Azt jelzi, hogy a virtuális gép futtatja a Linux operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="84149-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84149-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="84149-119">-LocalPath</span></span>
<span data-ttu-id="84149-120">A rendszerindítási diagnosztika adatainak helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84149-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84149-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84149-121">-Name</span></span>
<span data-ttu-id="84149-122">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag diagnosztikai adatot kap.</span><span class="sxs-lookup"><span data-stu-id="84149-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84149-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84149-123">-ResourceGroupName</span></span>
<span data-ttu-id="84149-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84149-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="84149-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="84149-125">-Windows</span></span>
<span data-ttu-id="84149-126">Azt jelzi, hogy a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="84149-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84149-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84149-127">CommonParameters</span></span>
<span data-ttu-id="84149-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84149-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84149-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="84149-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84149-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84149-130">INPUTS</span></span>

### <span data-ttu-id="84149-131">System. String</span><span class="sxs-lookup"><span data-stu-id="84149-131">System.String</span></span>

## <span data-ttu-id="84149-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84149-132">OUTPUTS</span></span>

### <span data-ttu-id="84149-133">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="84149-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="84149-134">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="84149-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="84149-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84149-135">NOTES</span></span>

## <span data-ttu-id="84149-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84149-136">RELATED LINKS</span></span>

[<span data-ttu-id="84149-137">Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="84149-137">Set-AzVMBootDiagnostics</span></span>](./Set-AzVMBootDiagnostics.md)


