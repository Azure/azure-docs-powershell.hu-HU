---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494548"
---
# <span data-ttu-id="bb5f5-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb5f5-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="bb5f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5f5-103">A virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb5f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb5f5-104">SYNTAX</span></span>

### <span data-ttu-id="bb5f5-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb5f5-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="bb5f5-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb5f5-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## <span data-ttu-id="bb5f5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb5f5-107">DESCRIPTION</span></span>
<span data-ttu-id="bb5f5-108">A **set-AzureRmVMBootDiagnostics** parancsmag a virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="bb5f5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bb5f5-109">EXAMPLES</span></span>

### <span data-ttu-id="bb5f5-110">1. példa: a boot Diagnostics engedélyezése</span><span class="sxs-lookup"><span data-stu-id="bb5f5-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

<span data-ttu-id="bb5f5-111">Az első parancs a **Get-AzureRmVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="bb5f5-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="bb5f5-113">A második parancs engedélyezi a rendszerindítási diagnosztikát a virtuális gép számára a $VMban.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="bb5f5-114">A diagnosztikai adatait a rendszer a megadott fiókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="bb5f5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb5f5-115">PARAMETERS</span></span>

### <span data-ttu-id="bb5f5-116">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="bb5f5-116">-Disable</span></span>
<span data-ttu-id="bb5f5-117">Jelzi, hogy ez a parancsmag letiltja a virtuális gép rendszerindítási diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-117">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5f5-118">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="bb5f5-118">-Enable</span></span>
<span data-ttu-id="bb5f5-119">Jelzi, hogy ez a parancsmag engedélyezi a virtuális gép rendszerindítási diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-119">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb5f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb5f5-121">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-121">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5f5-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bb5f5-122">-StorageAccountName</span></span>
<span data-ttu-id="bb5f5-123">Annak a tárolási fióknak a nevét adja meg, amelybe menteni szeretné a rendszerindítási diagnosztikai adatait.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-123">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5f5-124">-VM</span><span class="sxs-lookup"><span data-stu-id="bb5f5-124">-VM</span></span>
<span data-ttu-id="bb5f5-125">Azt a virtuális gépet adja meg, amelyhez ez a parancsmag a rendszerindítási diagnosztikát módosítja.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-125">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="bb5f5-126">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-126">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5f5-127">CommonParameters</span></span>
<span data-ttu-id="bb5f5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb5f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5f5-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5f5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5f5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb5f5-130">INPUTS</span></span>

### <span data-ttu-id="bb5f5-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="bb5f5-131">None</span></span>
<span data-ttu-id="bb5f5-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb5f5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb5f5-133">OUTPUTS</span></span>

## <span data-ttu-id="bb5f5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb5f5-134">NOTES</span></span>

## <span data-ttu-id="bb5f5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb5f5-135">RELATED LINKS</span></span>

[<span data-ttu-id="bb5f5-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bb5f5-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="bb5f5-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="bb5f5-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


