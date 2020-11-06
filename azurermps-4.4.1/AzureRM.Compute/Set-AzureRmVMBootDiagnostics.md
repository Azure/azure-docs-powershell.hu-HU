---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 32f5973668ca03dedb22b05186eda83002167648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492508"
---
# <span data-ttu-id="7413a-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7413a-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="7413a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7413a-102">SYNOPSIS</span></span>
<span data-ttu-id="7413a-103">A virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="7413a-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7413a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7413a-104">SYNTAX</span></span>

### <span data-ttu-id="7413a-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7413a-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7413a-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7413a-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7413a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7413a-107">DESCRIPTION</span></span>
<span data-ttu-id="7413a-108">A **set-AzureRmVMBootDiagnostics** parancsmag a virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="7413a-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="7413a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7413a-109">EXAMPLES</span></span>

### <span data-ttu-id="7413a-110">1. példa: a boot Diagnostics engedélyezése</span><span class="sxs-lookup"><span data-stu-id="7413a-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="7413a-111">Az első parancs a **Get-AzureRmVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="7413a-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="7413a-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7413a-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="7413a-113">A második parancs engedélyezi a rendszerindítási diagnosztikát a virtuális gép számára a $VMban.</span><span class="sxs-lookup"><span data-stu-id="7413a-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="7413a-114">A diagnosztikai adatait a rendszer a megadott fiókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7413a-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="7413a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7413a-115">PARAMETERS</span></span>

### <span data-ttu-id="7413a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7413a-116">-DefaultProfile</span></span>
<span data-ttu-id="7413a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7413a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7413a-118">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="7413a-118">-Disable</span></span>
<span data-ttu-id="7413a-119">Jelzi, hogy ez a parancsmag letiltja a virtuális gép rendszerindítási diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="7413a-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="7413a-120">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="7413a-120">-Enable</span></span>
<span data-ttu-id="7413a-121">Jelzi, hogy ez a parancsmag engedélyezi a virtuális gép rendszerindítási diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="7413a-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="7413a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7413a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7413a-123">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7413a-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7413a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7413a-124">-StorageAccountName</span></span>
<span data-ttu-id="7413a-125">Annak a tárolási fióknak a nevét adja meg, amelybe menteni szeretné a rendszerindítási diagnosztikai adatait.</span><span class="sxs-lookup"><span data-stu-id="7413a-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="7413a-126">-VM</span><span class="sxs-lookup"><span data-stu-id="7413a-126">-VM</span></span>
<span data-ttu-id="7413a-127">Azt a virtuális gépet adja meg, amelyhez ez a parancsmag a rendszerindítási diagnosztikát módosítja.</span><span class="sxs-lookup"><span data-stu-id="7413a-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="7413a-128">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7413a-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="7413a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7413a-129">CommonParameters</span></span>
<span data-ttu-id="7413a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7413a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7413a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7413a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7413a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7413a-132">INPUTS</span></span>

## <span data-ttu-id="7413a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7413a-133">OUTPUTS</span></span>

## <span data-ttu-id="7413a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7413a-134">NOTES</span></span>

## <span data-ttu-id="7413a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7413a-135">RELATED LINKS</span></span>

[<span data-ttu-id="7413a-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7413a-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7413a-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7413a-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


