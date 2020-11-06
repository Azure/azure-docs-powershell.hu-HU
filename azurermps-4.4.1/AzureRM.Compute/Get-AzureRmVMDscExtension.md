---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: ea54fc227fb32fe945a7a5ccc33133fc3b1d98a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500899"
---
# <span data-ttu-id="0a39f-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0a39f-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="0a39f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a39f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a39f-103">Egy adott virtuális gépen a DSC bővítmény beállításait kapja.</span><span class="sxs-lookup"><span data-stu-id="0a39f-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a39f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a39f-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a39f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a39f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a39f-106">A **Get-AzureRmVMDscExtension** parancsmag az adott virtuális gépen a kívánt állapot-konfiguráció (DSC) kiterjesztésének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0a39f-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="0a39f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0a39f-107">EXAMPLES</span></span>

### <span data-ttu-id="0a39f-108">Példa 1: a DSC kiterjesztés beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="0a39f-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="0a39f-109">Ez a parancs a DSC nevű bővítmény beállítását a VM07 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0a39f-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="0a39f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a39f-110">PARAMETERS</span></span>

### <span data-ttu-id="0a39f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a39f-111">-DefaultProfile</span></span>
<span data-ttu-id="0a39f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a39f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a39f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a39f-113">-Name</span></span>
<span data-ttu-id="0a39f-114">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a39f-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="0a39f-115">A Set-AzureRmVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzureRmVMDscExtension** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="0a39f-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="0a39f-116">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a **set-AzureRmVMDscExtension** parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="0a39f-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="0a39f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a39f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a39f-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a39f-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0a39f-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="0a39f-119">-Status</span></span>
<span data-ttu-id="0a39f-120">Jelzi, hogy ez a parancsmag a DSC bővítmény példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="0a39f-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a39f-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="0a39f-121">-VMName</span></span>
<span data-ttu-id="0a39f-122">Annak a virtuális gépnek a neve, amelyhez a parancsmag a DSC kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="0a39f-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a39f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a39f-123">CommonParameters</span></span>
<span data-ttu-id="0a39f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a39f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a39f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a39f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a39f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a39f-126">INPUTS</span></span>

## <span data-ttu-id="0a39f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a39f-127">OUTPUTS</span></span>

### <span data-ttu-id="0a39f-128">Microsoft. Azure. commands. számítási. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0a39f-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="0a39f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a39f-129">NOTES</span></span>

## <span data-ttu-id="0a39f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a39f-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a39f-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0a39f-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="0a39f-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0a39f-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


