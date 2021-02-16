---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144955"
---
# <span data-ttu-id="0929c-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0929c-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="0929c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0929c-102">SYNOPSIS</span></span>
<span data-ttu-id="0929c-103">Információkat kap egy Bővítmény bővítményről.</span><span class="sxs-lookup"><span data-stu-id="0929c-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="0929c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0929c-104">SYNTAX</span></span>

### <span data-ttu-id="0929c-105">Linux</span><span class="sxs-lookup"><span data-stu-id="0929c-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0929c-106">Windows</span><span class="sxs-lookup"><span data-stu-id="0929c-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0929c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0929c-107">DESCRIPTION</span></span>
<span data-ttu-id="0929c-108">A **Get-AzVMChefExtension** parancsmag információkat kap egy virtuális gépre telepített Bővítmény bővítményről.</span><span class="sxs-lookup"><span data-stu-id="0929c-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="0929c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0929c-109">EXAMPLES</span></span>

### <span data-ttu-id="0929c-110">1. példa: A Bővítmény bővítmény részleteinek le szerezze a Windows virtuális gépét</span><span class="sxs-lookup"><span data-stu-id="0929c-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="0929c-111">Ez a parancs a Bővítmény bővítményt egy WindowsVM001 nevű Windows virtuális gépből kapja, amely az ResourceGroup001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="0929c-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0929c-112">2. példa: A Kernel bővítmény részleteinek lekérte egy Linux-virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="0929c-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="0929c-113">Ez a parancs egy LinuxVM001 nevű Linux virtuális gépRől kapja meg a Bővítmény bővítményt, amely az ResourceGroup002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="0929c-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0929c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0929c-114">PARAMETERS</span></span>

### <span data-ttu-id="0929c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0929c-115">-DefaultProfile</span></span>
<span data-ttu-id="0929c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0929c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0929c-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0929c-117">-Linux</span></span>
<span data-ttu-id="0929c-118">Azt jelzi, hogy ez a parancsmag linuxos virtuális gépen működik.</span><span class="sxs-lookup"><span data-stu-id="0929c-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0929c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0929c-119">-Name</span></span>
<span data-ttu-id="0929c-120">A Bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0929c-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="0929c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0929c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0929c-122">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0929c-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="0929c-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="0929c-123">-Status</span></span>
<span data-ttu-id="0929c-124">Azt jelzi, hogy ez a parancsmag csak a Bővítmény bővítmény példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0929c-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="0929c-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="0929c-125">-VMName</span></span>
<span data-ttu-id="0929c-126">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0929c-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="0929c-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="0929c-127">-Windows</span></span>
<span data-ttu-id="0929c-128">Azt jelzi, hogy ez a parancsmag egy windowsos virtuális géphez való.</span><span class="sxs-lookup"><span data-stu-id="0929c-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0929c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0929c-129">CommonParameters</span></span>
<span data-ttu-id="0929c-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0929c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0929c-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0929c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0929c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0929c-132">INPUTS</span></span>

### <span data-ttu-id="0929c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0929c-133">System.String</span></span>

### <span data-ttu-id="0929c-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0929c-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0929c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0929c-135">OUTPUTS</span></span>

### <span data-ttu-id="0929c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0929c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="0929c-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0929c-137">NOTES</span></span>

## <span data-ttu-id="0929c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0929c-138">RELATED LINKS</span></span>

[<span data-ttu-id="0929c-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0929c-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="0929c-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0929c-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


