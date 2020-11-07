---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextension
schema: 2.0.0
ms.openlocfilehash: 0954bcb395cf4a0dcf64dac178b1168ee1abd59b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849402"
---
# <span data-ttu-id="e43ca-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e43ca-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="e43ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e43ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e43ca-103">Egy adott virtuális gépen a DSC bővítmény beállításait kapja.</span><span class="sxs-lookup"><span data-stu-id="e43ca-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e43ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e43ca-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e43ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e43ca-106">A **Get-AzureRmVMDscExtension** parancsmag az adott virtuális gépen a kívánt állapot-konfiguráció (DSC) kiterjesztésének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e43ca-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="e43ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e43ca-107">EXAMPLES</span></span>

### <span data-ttu-id="e43ca-108">Példa 1: a DSC kiterjesztés beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="e43ca-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="e43ca-109">Ez a parancs a DSC nevű bővítmény beállítását a VM07 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e43ca-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="e43ca-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e43ca-110">PARAMETERS</span></span>

### <span data-ttu-id="e43ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43ca-111">-DefaultProfile</span></span>
<span data-ttu-id="e43ca-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e43ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43ca-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e43ca-113">-Name</span></span>
<span data-ttu-id="e43ca-114">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e43ca-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e43ca-115">A Set-AzureRmVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzureRmVMDscExtension** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="e43ca-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="e43ca-116">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a **set-AzureRmVMDscExtension** parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="e43ca-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="e43ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="e43ca-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e43ca-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43ca-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="e43ca-119">-Status</span></span>
<span data-ttu-id="e43ca-120">Jelzi, hogy ez a parancsmag a DSC bővítmény példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="e43ca-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43ca-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="e43ca-121">-VMName</span></span>
<span data-ttu-id="e43ca-122">Annak a virtuális gépnek a neve, amelyhez a parancsmag a DSC kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="e43ca-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43ca-123">CommonParameters</span></span>
<span data-ttu-id="e43ca-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e43ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43ca-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e43ca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43ca-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e43ca-126">INPUTS</span></span>

### <span data-ttu-id="e43ca-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="e43ca-127">None</span></span>
<span data-ttu-id="e43ca-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e43ca-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e43ca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e43ca-129">OUTPUTS</span></span>

### <span data-ttu-id="e43ca-130">Microsoft. Azure. commands. számítási. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="e43ca-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="e43ca-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e43ca-131">NOTES</span></span>

## <span data-ttu-id="e43ca-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e43ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="e43ca-133">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e43ca-133">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="e43ca-134">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e43ca-134">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


