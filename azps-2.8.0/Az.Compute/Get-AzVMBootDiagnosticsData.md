---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: ee210b5b9408f3de2b9e92213fafe4846ea8c3e1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407097"
---
# <span data-ttu-id="cffe4-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cffe4-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="cffe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cffe4-102">SYNOPSIS</span></span>
<span data-ttu-id="cffe4-103">Indítási diagnosztikai adatokat kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cffe4-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="cffe4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cffe4-104">SYNTAX</span></span>

### <span data-ttu-id="cffe4-105">WindowsParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cffe4-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cffe4-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="cffe4-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cffe4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cffe4-107">DESCRIPTION</span></span>
<span data-ttu-id="cffe4-108">A **Get-AzVMBootDiagnosticsData** parancsmag indítási diagnosztikai adatokat kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cffe4-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="cffe4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cffe4-109">EXAMPLES</span></span>

### <span data-ttu-id="cffe4-110">1. példa: Indítási diagnosztikai adatok betöltése</span><span class="sxs-lookup"><span data-stu-id="cffe4-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="cffe4-111">Ez a parancs a ContosoVM07 nevű virtuális gép indítási diagnosztikai adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="cffe4-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="cffe4-112">Ez a virtuális gép a Windows operációs rendszert futtatja.</span><span class="sxs-lookup"><span data-stu-id="cffe4-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="cffe4-113">A parancs a megadott helyi elérési úton tárolja az adatokat.</span><span class="sxs-lookup"><span data-stu-id="cffe4-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="cffe4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cffe4-114">PARAMETERS</span></span>

### <span data-ttu-id="cffe4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffe4-115">-DefaultProfile</span></span>
<span data-ttu-id="cffe4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cffe4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cffe4-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="cffe4-117">-Linux</span></span>
<span data-ttu-id="cffe4-118">Azt jelzi, hogy a virtuális gép a Linux operációs rendszert futtatja.</span><span class="sxs-lookup"><span data-stu-id="cffe4-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="cffe4-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="cffe4-119">-LocalPath</span></span>
<span data-ttu-id="cffe4-120">A rendszerindításkor használt diagnosztikai adatok helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cffe4-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="cffe4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cffe4-121">-Name</span></span>
<span data-ttu-id="cffe4-122">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag diagnosztikai adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="cffe4-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="cffe4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cffe4-123">-ResourceGroupName</span></span>
<span data-ttu-id="cffe4-124">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cffe4-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cffe4-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="cffe4-125">-Windows</span></span>
<span data-ttu-id="cffe4-126">Azt jelzi, hogy a virtuális gép a Windows operációs rendszert futtatja.</span><span class="sxs-lookup"><span data-stu-id="cffe4-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="cffe4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffe4-127">CommonParameters</span></span>
<span data-ttu-id="cffe4-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cffe4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffe4-129">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cffe4-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffe4-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cffe4-130">INPUTS</span></span>

### <span data-ttu-id="cffe4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cffe4-131">System.String</span></span>

## <span data-ttu-id="cffe4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cffe4-132">OUTPUTS</span></span>

### <span data-ttu-id="cffe4-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cffe4-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="cffe4-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="cffe4-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="cffe4-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cffe4-135">NOTES</span></span>

## <span data-ttu-id="cffe4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cffe4-136">RELATED LINKS</span></span>

[<span data-ttu-id="cffe4-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cffe4-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


