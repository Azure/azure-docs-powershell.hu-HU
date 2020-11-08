---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183082"
---
# <span data-ttu-id="17bd2-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="17bd2-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="17bd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="17bd2-103">A virtuálisgép-készlet rendszerindítási diagnosztikai profiljának beállítása.</span><span class="sxs-lookup"><span data-stu-id="17bd2-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="17bd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17bd2-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17bd2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="17bd2-106">A virtuálisgép-készlet rendszerindítási diagnosztikai profiljának beállítása.</span><span class="sxs-lookup"><span data-stu-id="17bd2-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="17bd2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="17bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="17bd2-108">Példa 1: a rendszerindítási diagnosztikai profil tulajdonság beállítása VMSS</span><span class="sxs-lookup"><span data-stu-id="17bd2-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="17bd2-109">Ez a parancs beállítja a rendszerindítási diagnosztikai profil tulajdonságot a ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="17bd2-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="17bd2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="17bd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bd2-111">-DefaultProfile</span></span>
<span data-ttu-id="17bd2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17bd2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17bd2-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="17bd2-113">-Enabled</span></span>
<span data-ttu-id="17bd2-114">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="17bd2-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17bd2-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="17bd2-115">-StorageUri</span></span>
<span data-ttu-id="17bd2-116">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="17bd2-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17bd2-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17bd2-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="17bd2-118">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="17bd2-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="17bd2-119">Az objektum létrehozásához az New-AzVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="17bd2-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17bd2-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17bd2-120">-Confirm</span></span>
<span data-ttu-id="17bd2-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17bd2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bd2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bd2-122">-WhatIf</span></span>
<span data-ttu-id="17bd2-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17bd2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17bd2-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17bd2-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bd2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bd2-125">CommonParameters</span></span>
<span data-ttu-id="17bd2-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17bd2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bd2-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="17bd2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bd2-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17bd2-128">INPUTS</span></span>

### <span data-ttu-id="17bd2-129">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17bd2-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="17bd2-130">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17bd2-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17bd2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="17bd2-131">System.String</span></span>

## <span data-ttu-id="17bd2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17bd2-132">OUTPUTS</span></span>

### <span data-ttu-id="17bd2-133">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17bd2-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="17bd2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17bd2-134">NOTES</span></span>

## <span data-ttu-id="17bd2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17bd2-135">RELATED LINKS</span></span>
