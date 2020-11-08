---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: c56c9e586b0089311477fc12b6624c74321f9a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015057"
---
# <span data-ttu-id="fce77-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="fce77-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="fce77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fce77-102">SYNOPSIS</span></span>
<span data-ttu-id="fce77-103">Rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fce77-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="fce77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fce77-104">SYNTAX</span></span>

### <span data-ttu-id="fce77-105">WindowsParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fce77-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fce77-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="fce77-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fce77-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fce77-107">DESCRIPTION</span></span>
<span data-ttu-id="fce77-108">A **Get-AzVMBootDiagnosticsData** parancsmag rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fce77-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="fce77-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fce77-109">EXAMPLES</span></span>

### <span data-ttu-id="fce77-110">1. példa: a rendszerindítási diagnosztika adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="fce77-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="fce77-111">Ez a parancs a ContosoVM07 nevű virtuális gép rendszerindítási diagnosztikai értékeit kapja.</span><span class="sxs-lookup"><span data-stu-id="fce77-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="fce77-112">Ez a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="fce77-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="fce77-113">A parancs a megadott helyi elérési utakban tárolja az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="fce77-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="fce77-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fce77-114">PARAMETERS</span></span>

### <span data-ttu-id="fce77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce77-115">-DefaultProfile</span></span>
<span data-ttu-id="fce77-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fce77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fce77-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="fce77-117">-Linux</span></span>
<span data-ttu-id="fce77-118">Azt jelzi, hogy a virtuális gép futtatja a Linux operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="fce77-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="fce77-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="fce77-119">-LocalPath</span></span>
<span data-ttu-id="fce77-120">A rendszerindítási diagnosztika adatainak helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fce77-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="fce77-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fce77-121">-Name</span></span>
<span data-ttu-id="fce77-122">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag diagnosztikai adatot kap.</span><span class="sxs-lookup"><span data-stu-id="fce77-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="fce77-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce77-123">-ResourceGroupName</span></span>
<span data-ttu-id="fce77-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fce77-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fce77-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="fce77-125">-Windows</span></span>
<span data-ttu-id="fce77-126">Azt jelzi, hogy a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="fce77-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="fce77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce77-127">CommonParameters</span></span>
<span data-ttu-id="fce77-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fce77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce77-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fce77-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce77-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fce77-130">INPUTS</span></span>

### <span data-ttu-id="fce77-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fce77-131">System.String</span></span>

## <span data-ttu-id="fce77-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fce77-132">OUTPUTS</span></span>

### <span data-ttu-id="fce77-133">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fce77-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fce77-134">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="fce77-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="fce77-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fce77-135">NOTES</span></span>

## <span data-ttu-id="fce77-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fce77-136">RELATED LINKS</span></span>

[<span data-ttu-id="fce77-137">Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fce77-137">Set-AzVMBootDiagnostics</span></span>](./Set-AzVMBootDiagnostics.md)


