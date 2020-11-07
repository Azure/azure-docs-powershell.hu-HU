---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 7ec034ed0d84b0c45486d17adbdb5c0a152d27b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667220"
---
# <span data-ttu-id="0ad56-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0ad56-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="0ad56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ad56-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad56-103">A virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="0ad56-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="0ad56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ad56-104">SYNTAX</span></span>

### <span data-ttu-id="0ad56-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0ad56-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad56-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0ad56-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad56-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ad56-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad56-108">A **set-AzVMBootDiagnostic** parancsmag a virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="0ad56-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="0ad56-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ad56-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad56-110">1. példa: a boot Diagnostics engedélyezése</span><span class="sxs-lookup"><span data-stu-id="0ad56-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="0ad56-111">Az első parancs a **Get-AzVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="0ad56-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="0ad56-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ad56-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="0ad56-113">A második parancs engedélyezi a rendszerindítási diagnosztikát a virtuális gép számára a $VMban.</span><span class="sxs-lookup"><span data-stu-id="0ad56-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="0ad56-114">A diagnosztikai adatait a rendszer a megadott fiókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ad56-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="0ad56-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ad56-115">PARAMETERS</span></span>

### <span data-ttu-id="0ad56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad56-116">-DefaultProfile</span></span>
<span data-ttu-id="0ad56-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ad56-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad56-118">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="0ad56-118">-Disable</span></span>
<span data-ttu-id="0ad56-119">Jelzi, hogy ez a parancsmag letiltja a virtuális gép rendszerindítási diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="0ad56-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad56-120">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="0ad56-120">-Enable</span></span>
<span data-ttu-id="0ad56-121">Jelzi, hogy ez a parancsmag engedélyezi a virtuális gép rendszerindítási diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="0ad56-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad56-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ad56-123">A tárolási fiók erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ad56-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad56-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ad56-124">-StorageAccountName</span></span>
<span data-ttu-id="0ad56-125">Annak a tárolási fióknak a nevét adja meg, amelybe menteni szeretné a rendszerindítási diagnosztikai adatait.</span><span class="sxs-lookup"><span data-stu-id="0ad56-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad56-126">-VM</span><span class="sxs-lookup"><span data-stu-id="0ad56-126">-VM</span></span>
<span data-ttu-id="0ad56-127">Azt a virtuális gépet adja meg, amelyhez ez a parancsmag a rendszerindítási diagnosztikát módosítja.</span><span class="sxs-lookup"><span data-stu-id="0ad56-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="0ad56-128">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0ad56-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad56-129">CommonParameters</span></span>
<span data-ttu-id="0ad56-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ad56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad56-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ad56-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad56-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ad56-132">INPUTS</span></span>

### <span data-ttu-id="0ad56-133">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0ad56-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0ad56-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad56-134">System.String</span></span>

## <span data-ttu-id="0ad56-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ad56-135">OUTPUTS</span></span>

### <span data-ttu-id="0ad56-136">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0ad56-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0ad56-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ad56-137">NOTES</span></span>

## <span data-ttu-id="0ad56-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ad56-138">RELATED LINKS</span></span>

[<span data-ttu-id="0ad56-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0ad56-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0ad56-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0ad56-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


