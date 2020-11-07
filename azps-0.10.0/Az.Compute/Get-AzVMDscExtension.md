---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 70f06718c2d96e11b46842e4f39af26d3e29c2f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844602"
---
# <span data-ttu-id="e1f52-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e1f52-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="e1f52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1f52-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f52-103">Egy adott virtuális gépen a DSC bővítmény beállításait kapja.</span><span class="sxs-lookup"><span data-stu-id="e1f52-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="e1f52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1f52-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1f52-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f52-106">A **Get-AzVMDscExtension** parancsmag az adott virtuális gépen a kívánt állapot-konfiguráció (DSC) kiterjesztésének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e1f52-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="e1f52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1f52-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f52-108">Példa 1: a DSC kiterjesztés beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="e1f52-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="e1f52-109">Ez a parancs a DSC nevű bővítmény beállítását a VM07 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e1f52-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="e1f52-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1f52-110">PARAMETERS</span></span>

### <span data-ttu-id="e1f52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f52-111">-DefaultProfile</span></span>
<span data-ttu-id="e1f52-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1f52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1f52-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1f52-113">-Name</span></span>
<span data-ttu-id="e1f52-114">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1f52-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e1f52-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzVMDscExtension** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="e1f52-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="e1f52-116">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a **set-AzVMDscExtension** parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="e1f52-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="e1f52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f52-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1f52-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1f52-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e1f52-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="e1f52-119">-Status</span></span>
<span data-ttu-id="e1f52-120">Jelzi, hogy ez a parancsmag a DSC bővítmény példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="e1f52-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="e1f52-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="e1f52-121">-VMName</span></span>
<span data-ttu-id="e1f52-122">Annak a virtuális gépnek a neve, amelyhez a parancsmag a DSC kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="e1f52-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="e1f52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f52-123">CommonParameters</span></span>
<span data-ttu-id="e1f52-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1f52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f52-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f52-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f52-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1f52-126">INPUTS</span></span>

### <span data-ttu-id="e1f52-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1f52-127">None</span></span>
<span data-ttu-id="e1f52-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e1f52-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1f52-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1f52-129">OUTPUTS</span></span>

### <span data-ttu-id="e1f52-130">Microsoft. Azure. commands. számítási. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="e1f52-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="e1f52-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1f52-131">NOTES</span></span>

## <span data-ttu-id="e1f52-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1f52-132">RELATED LINKS</span></span>

[<span data-ttu-id="e1f52-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e1f52-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="e1f52-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e1f52-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


