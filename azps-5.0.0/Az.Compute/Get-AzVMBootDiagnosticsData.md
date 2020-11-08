---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195117"
---
# <span data-ttu-id="a1d7a-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a1d7a-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="a1d7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d7a-103">Rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="a1d7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1d7a-104">SYNTAX</span></span>

### <span data-ttu-id="a1d7a-105">WindowsParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1d7a-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1d7a-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="a1d7a-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1d7a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="a1d7a-108">A **Get-AzVMBootDiagnosticsData** parancsmag rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="a1d7a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a1d7a-109">EXAMPLES</span></span>

### <span data-ttu-id="a1d7a-110">1. példa: a rendszerindítási diagnosztika adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="a1d7a-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="a1d7a-111">Ez a parancs a ContosoVM07 nevű virtuális gép rendszerindítási diagnosztikai értékeit kapja.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="a1d7a-112">Ez a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="a1d7a-113">A parancs a megadott helyi elérési utakban tárolja az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="a1d7a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1d7a-114">PARAMETERS</span></span>

### <span data-ttu-id="a1d7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d7a-115">-DefaultProfile</span></span>
<span data-ttu-id="a1d7a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1d7a-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="a1d7a-117">-Linux</span></span>
<span data-ttu-id="a1d7a-118">Azt jelzi, hogy a virtuális gép futtatja a Linux operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="a1d7a-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="a1d7a-119">-LocalPath</span></span>
<span data-ttu-id="a1d7a-120">A rendszerindítási diagnosztika adatainak helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="a1d7a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1d7a-121">-Name</span></span>
<span data-ttu-id="a1d7a-122">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag diagnosztikai adatot kap.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="a1d7a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d7a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1d7a-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a1d7a-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="a1d7a-125">-Windows</span></span>
<span data-ttu-id="a1d7a-126">Azt jelzi, hogy a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="a1d7a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d7a-127">CommonParameters</span></span>
<span data-ttu-id="a1d7a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1d7a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d7a-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1d7a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d7a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d7a-130">INPUTS</span></span>

### <span data-ttu-id="a1d7a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d7a-131">System.String</span></span>

## <span data-ttu-id="a1d7a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d7a-132">OUTPUTS</span></span>

### <span data-ttu-id="a1d7a-133">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a1d7a-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a1d7a-134">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="a1d7a-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="a1d7a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1d7a-135">NOTES</span></span>

## <span data-ttu-id="a1d7a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1d7a-136">RELATED LINKS</span></span>

[<span data-ttu-id="a1d7a-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a1d7a-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


