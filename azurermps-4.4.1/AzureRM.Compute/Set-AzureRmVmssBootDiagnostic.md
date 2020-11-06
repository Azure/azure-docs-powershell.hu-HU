---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: dcfc0fcf2901f7f604e4d39e330db61633ef0dee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492497"
---
# <span data-ttu-id="6442a-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6442a-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="6442a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6442a-102">SYNOPSIS</span></span>
<span data-ttu-id="6442a-103">A virtuálisgép-készlet rendszerindítási diagnosztikai profiljának beállítása.</span><span class="sxs-lookup"><span data-stu-id="6442a-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6442a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6442a-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6442a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6442a-105">DESCRIPTION</span></span>
<span data-ttu-id="6442a-106">A virtuálisgép-készlet rendszerindítási diagnosztikai profiljának beállítása.</span><span class="sxs-lookup"><span data-stu-id="6442a-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="6442a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6442a-107">EXAMPLES</span></span>

### <span data-ttu-id="6442a-108">Példa 1: a rendszerindítási diagnosztikai profil tulajdonság beállítása VMSS</span><span class="sxs-lookup"><span data-stu-id="6442a-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="6442a-109">Ez a parancs beállítja a rendszerindítási diagnosztikai profil tulajdonságot a ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="6442a-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6442a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6442a-110">PARAMETERS</span></span>

### <span data-ttu-id="6442a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6442a-111">-DefaultProfile</span></span>
<span data-ttu-id="6442a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6442a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6442a-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="6442a-113">-Enabled</span></span>
<span data-ttu-id="6442a-114">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="6442a-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6442a-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="6442a-115">-StorageUri</span></span>
<span data-ttu-id="6442a-116">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6442a-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="6442a-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6442a-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6442a-118">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6442a-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="6442a-119">Az objektum létrehozásához az New-AzureRmVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="6442a-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6442a-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6442a-120">-Confirm</span></span>
<span data-ttu-id="6442a-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6442a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6442a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6442a-122">-WhatIf</span></span>
<span data-ttu-id="6442a-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6442a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6442a-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6442a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6442a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6442a-125">CommonParameters</span></span>
<span data-ttu-id="6442a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6442a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6442a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6442a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6442a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6442a-128">INPUTS</span></span>

### <span data-ttu-id="6442a-129">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6442a-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="6442a-130">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="6442a-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="6442a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6442a-131">OUTPUTS</span></span>

### <span data-ttu-id="6442a-132">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6442a-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="6442a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6442a-133">NOTES</span></span>

## <span data-ttu-id="6442a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6442a-134">RELATED LINKS</span></span>

