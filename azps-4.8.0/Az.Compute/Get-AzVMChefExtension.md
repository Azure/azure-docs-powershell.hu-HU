---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024142"
---
# <span data-ttu-id="6ee10-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6ee10-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="6ee10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ee10-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee10-103">Információt kap a szakács kibővítéséről.</span><span class="sxs-lookup"><span data-stu-id="6ee10-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="6ee10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ee10-104">SYNTAX</span></span>

### <span data-ttu-id="6ee10-105">Linux</span><span class="sxs-lookup"><span data-stu-id="6ee10-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ee10-106">Windows</span><span class="sxs-lookup"><span data-stu-id="6ee10-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ee10-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ee10-107">DESCRIPTION</span></span>
<span data-ttu-id="6ee10-108">A **Get-AzVMChefExtension** parancsmag a virtuális gépre telepített Chef-bővítményekről tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="6ee10-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="6ee10-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6ee10-109">EXAMPLES</span></span>

### <span data-ttu-id="6ee10-110">Példa 1: a séf kibővítésének részletei a Windows Virtual Machine alkalmazásban</span><span class="sxs-lookup"><span data-stu-id="6ee10-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="6ee10-111">Ez a parancs a Chef bővítményt egy olyan Windows Virtual Machine-WindowsVM001 kapja, amely az ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="6ee10-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="6ee10-112">2. példa: a séf-kiterjesztés részleteinek beszerzése egy linuxos virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="6ee10-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="6ee10-113">Ez a parancs a Chef kiterjesztését egy LinuxVM001 nevű linuxos virtuális gépről kapja, amely az ResourceGroup002 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="6ee10-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="6ee10-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ee10-114">PARAMETERS</span></span>

### <span data-ttu-id="6ee10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee10-115">-DefaultProfile</span></span>
<span data-ttu-id="6ee10-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ee10-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ee10-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="6ee10-117">-Linux</span></span>
<span data-ttu-id="6ee10-118">Jelzi, hogy ez a parancsmag egy linuxos virtuális gépen működik.</span><span class="sxs-lookup"><span data-stu-id="6ee10-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="6ee10-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ee10-119">-Name</span></span>
<span data-ttu-id="6ee10-120">A Szakácsi mellék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ee10-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="6ee10-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee10-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ee10-122">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ee10-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="6ee10-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="6ee10-123">-Status</span></span>
<span data-ttu-id="6ee10-124">Azt jelzi, hogy ez a parancsmag csak a séf bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6ee10-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="6ee10-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="6ee10-125">-VMName</span></span>
<span data-ttu-id="6ee10-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ee10-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="6ee10-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="6ee10-127">-Windows</span></span>
<span data-ttu-id="6ee10-128">Jelzi, hogy ez a parancsmag egy Windows Virtual Machine-géphez van.</span><span class="sxs-lookup"><span data-stu-id="6ee10-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="6ee10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee10-129">CommonParameters</span></span>
<span data-ttu-id="6ee10-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ee10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee10-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ee10-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee10-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ee10-132">INPUTS</span></span>

### <span data-ttu-id="6ee10-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6ee10-133">System.String</span></span>

### <span data-ttu-id="6ee10-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ee10-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ee10-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ee10-135">OUTPUTS</span></span>

### <span data-ttu-id="6ee10-136">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6ee10-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="6ee10-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ee10-137">NOTES</span></span>

## <span data-ttu-id="6ee10-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ee10-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ee10-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6ee10-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="6ee10-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6ee10-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


