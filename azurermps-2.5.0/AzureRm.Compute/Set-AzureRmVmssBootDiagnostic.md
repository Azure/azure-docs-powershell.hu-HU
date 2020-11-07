---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
ms.openlocfilehash: cca99d994380483465f9026ba8023cd92afc7e37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848322"
---
# <span data-ttu-id="2d063-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2d063-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="2d063-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d063-102">SYNOPSIS</span></span>
<span data-ttu-id="2d063-103">A virtuálisgép-készlet rendszerindítási diagnosztikai profiljának beállítása.</span><span class="sxs-lookup"><span data-stu-id="2d063-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d063-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d063-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d063-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d063-105">DESCRIPTION</span></span>
<span data-ttu-id="2d063-106">A virtuálisgép-készlet rendszerindítási diagnosztikai profiljának beállítása.</span><span class="sxs-lookup"><span data-stu-id="2d063-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="2d063-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d063-107">EXAMPLES</span></span>

### <span data-ttu-id="2d063-108">Példa 1: a rendszerindítási diagnosztikai profil tulajdonság beállítása VMSS</span><span class="sxs-lookup"><span data-stu-id="2d063-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="2d063-109">Ez a parancs beállítja a rendszerindítási diagnosztikai profil tulajdonságot a ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="2d063-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="2d063-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d063-110">PARAMETERS</span></span>

### <span data-ttu-id="2d063-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d063-111">-DefaultProfile</span></span>
<span data-ttu-id="2d063-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d063-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d063-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2d063-113">-Enabled</span></span>
<span data-ttu-id="2d063-114">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="2d063-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d063-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="2d063-115">-StorageUri</span></span>
<span data-ttu-id="2d063-116">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2d063-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d063-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d063-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2d063-118">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d063-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="2d063-119">Az objektum létrehozásához az New-AzureRmVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="2d063-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d063-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d063-120">-Confirm</span></span>
<span data-ttu-id="2d063-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d063-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d063-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d063-122">-WhatIf</span></span>
<span data-ttu-id="2d063-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d063-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d063-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d063-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d063-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d063-125">CommonParameters</span></span>
<span data-ttu-id="2d063-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d063-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d063-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d063-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d063-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d063-128">INPUTS</span></span>

### <span data-ttu-id="2d063-129">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d063-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="2d063-130">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="2d063-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="2d063-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d063-131">OUTPUTS</span></span>

### <span data-ttu-id="2d063-132">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d063-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="2d063-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d063-133">NOTES</span></span>

## <span data-ttu-id="2d063-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d063-134">RELATED LINKS</span></span>

