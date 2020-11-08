---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186474"
---
# <span data-ttu-id="4ac5c-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4ac5c-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="4ac5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ac5c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac5c-103">Az Analysis Services Server példányának felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="4ac5c-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="4ac5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ac5c-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ac5c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac5c-106">Az Suspend-AzAnalysisServicesServer parancsmag felfüggeszti az Analysis Services-kiszolgáló egy példányát.</span><span class="sxs-lookup"><span data-stu-id="4ac5c-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="4ac5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ac5c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ac5c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ac5c-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="4ac5c-109">Ez a parancs felfüggeszti a TestServer nevű aktív kiszolgálót a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="4ac5c-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4ac5c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ac5c-110">PARAMETERS</span></span>

### <span data-ttu-id="4ac5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac5c-111">-DefaultProfile</span></span>
<span data-ttu-id="4ac5c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ac5c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ac5c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ac5c-113">-Name</span></span>
<span data-ttu-id="4ac5c-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="4ac5c-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4ac5c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ac5c-115">-PassThru</span></span>
<span data-ttu-id="4ac5c-116">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="4ac5c-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="4ac5c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac5c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ac5c-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="4ac5c-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="4ac5c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ac5c-119">-Confirm</span></span>
<span data-ttu-id="4ac5c-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="4ac5c-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4ac5c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac5c-121">-WhatIf</span></span>
<span data-ttu-id="4ac5c-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="4ac5c-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4ac5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac5c-123">CommonParameters</span></span>
<span data-ttu-id="4ac5c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ac5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac5c-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac5c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac5c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ac5c-126">INPUTS</span></span>

### <span data-ttu-id="4ac5c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac5c-127">System.String</span></span>

## <span data-ttu-id="4ac5c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ac5c-128">OUTPUTS</span></span>

### <span data-ttu-id="4ac5c-129">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4ac5c-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="4ac5c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ac5c-130">NOTES</span></span>
<span data-ttu-id="4ac5c-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="4ac5c-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="4ac5c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ac5c-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ac5c-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4ac5c-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="4ac5c-134">Önéletrajz – AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4ac5c-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

