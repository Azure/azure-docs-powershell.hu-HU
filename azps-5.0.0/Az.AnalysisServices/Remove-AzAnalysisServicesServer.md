---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186481"
---
# <span data-ttu-id="7d7ad-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d7ad-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="7d7ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7d7ad-103">Az Analysis Services-kiszolgáló példányainak törlése</span><span class="sxs-lookup"><span data-stu-id="7d7ad-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="7d7ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d7ad-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d7ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d7ad-105">DESCRIPTION</span></span>
<span data-ttu-id="7d7ad-106">Az Remove-AzAnalysisServicesServer parancsmag törli az Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="7d7ad-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="7d7ad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7d7ad-107">EXAMPLES</span></span>

### <span data-ttu-id="7d7ad-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7d7ad-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="7d7ad-109">Ez a parancs eltávolítja a TestServer nevű kiszolgálót a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="7d7ad-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="7d7ad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d7ad-110">PARAMETERS</span></span>

### <span data-ttu-id="7d7ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d7ad-111">-DefaultProfile</span></span>
<span data-ttu-id="7d7ad-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d7ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d7ad-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d7ad-113">-Name</span></span>
<span data-ttu-id="7d7ad-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="7d7ad-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7d7ad-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d7ad-115">-PassThru</span></span>
<span data-ttu-id="7d7ad-116">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="7d7ad-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d7ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d7ad-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="7d7ad-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ad-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d7ad-119">-Confirm</span></span>
<span data-ttu-id="7d7ad-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="7d7ad-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7d7ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d7ad-121">-WhatIf</span></span>
<span data-ttu-id="7d7ad-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="7d7ad-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7d7ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d7ad-123">CommonParameters</span></span>
<span data-ttu-id="7d7ad-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d7ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d7ad-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d7ad-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d7ad-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d7ad-126">INPUTS</span></span>

### <span data-ttu-id="7d7ad-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7d7ad-127">System.String</span></span>

## <span data-ttu-id="7d7ad-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d7ad-128">OUTPUTS</span></span>

### <span data-ttu-id="7d7ad-129">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d7ad-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7d7ad-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d7ad-130">NOTES</span></span>
<span data-ttu-id="7d7ad-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="7d7ad-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="7d7ad-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d7ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="7d7ad-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d7ad-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="7d7ad-134">Új – AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d7ad-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)