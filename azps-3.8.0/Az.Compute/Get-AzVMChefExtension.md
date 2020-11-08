---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015055"
---
# <span data-ttu-id="f4db2-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f4db2-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="f4db2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4db2-102">SYNOPSIS</span></span>
<span data-ttu-id="f4db2-103">Információt kap a szakács kibővítéséről.</span><span class="sxs-lookup"><span data-stu-id="f4db2-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="f4db2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4db2-104">SYNTAX</span></span>

### <span data-ttu-id="f4db2-105">Linux</span><span class="sxs-lookup"><span data-stu-id="f4db2-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4db2-106">Windows</span><span class="sxs-lookup"><span data-stu-id="f4db2-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4db2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4db2-107">DESCRIPTION</span></span>
<span data-ttu-id="f4db2-108">A **Get-AzVMChefExtension** parancsmag a virtuális gépre telepített Chef-bővítményekről tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="f4db2-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="f4db2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f4db2-109">EXAMPLES</span></span>

### <span data-ttu-id="f4db2-110">Példa 1: a séf kibővítésének részletei a Windows Virtual Machine alkalmazásban</span><span class="sxs-lookup"><span data-stu-id="f4db2-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="f4db2-111">Ez a parancs a Chef bővítményt egy olyan Windows Virtual Machine-WindowsVM001 kapja, amely az ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="f4db2-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f4db2-112">2. példa: a séf-kiterjesztés részleteinek beszerzése egy linuxos virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="f4db2-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="f4db2-113">Ez a parancs a Chef kiterjesztését egy LinuxVM001 nevű linuxos virtuális gépről kapja, amely az ResourceGroup002 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="f4db2-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f4db2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4db2-114">PARAMETERS</span></span>

### <span data-ttu-id="f4db2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4db2-115">-DefaultProfile</span></span>
<span data-ttu-id="f4db2-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4db2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4db2-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="f4db2-117">-Linux</span></span>
<span data-ttu-id="f4db2-118">Jelzi, hogy ez a parancsmag egy linuxos virtuális gépen működik.</span><span class="sxs-lookup"><span data-stu-id="f4db2-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="f4db2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4db2-119">-Name</span></span>
<span data-ttu-id="f4db2-120">A Szakácsi mellék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4db2-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="f4db2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4db2-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4db2-122">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4db2-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f4db2-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f4db2-123">-Status</span></span>
<span data-ttu-id="f4db2-124">Azt jelzi, hogy ez a parancsmag csak a séf bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4db2-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="f4db2-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f4db2-125">-VMName</span></span>
<span data-ttu-id="f4db2-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4db2-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="f4db2-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="f4db2-127">-Windows</span></span>
<span data-ttu-id="f4db2-128">Jelzi, hogy ez a parancsmag egy Windows Virtual Machine-géphez van.</span><span class="sxs-lookup"><span data-stu-id="f4db2-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="f4db2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4db2-129">CommonParameters</span></span>
<span data-ttu-id="f4db2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4db2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4db2-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4db2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4db2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4db2-132">INPUTS</span></span>

### <span data-ttu-id="f4db2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f4db2-133">System.String</span></span>

### <span data-ttu-id="f4db2-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4db2-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4db2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4db2-135">OUTPUTS</span></span>

### <span data-ttu-id="f4db2-136">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f4db2-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="f4db2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4db2-137">NOTES</span></span>

## <span data-ttu-id="f4db2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4db2-138">RELATED LINKS</span></span>

[<span data-ttu-id="f4db2-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f4db2-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="f4db2-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f4db2-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


