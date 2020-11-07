---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: ba1c4c8267089d71a265de07b0f9508a24cf9b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668154"
---
# <span data-ttu-id="56164-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="56164-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="56164-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56164-102">SYNOPSIS</span></span>
<span data-ttu-id="56164-103">Az Analysis Services Server egy példányának folytatása</span><span class="sxs-lookup"><span data-stu-id="56164-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="56164-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56164-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56164-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56164-105">DESCRIPTION</span></span>
<span data-ttu-id="56164-106">Az Resume-AzAnalysisServicesServer parancsmag az Analysis Services Server egy példányát folytatja</span><span class="sxs-lookup"><span data-stu-id="56164-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="56164-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56164-107">EXAMPLES</span></span>

### <span data-ttu-id="56164-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56164-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="56164-109">Ez a parancs folytatja a TestServer nevű felfüggesztett kiszolgáló resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="56164-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="56164-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56164-110">PARAMETERS</span></span>

### <span data-ttu-id="56164-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56164-111">-DefaultProfile</span></span>
<span data-ttu-id="56164-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56164-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56164-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56164-113">-Name</span></span>
<span data-ttu-id="56164-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="56164-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="56164-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56164-115">-PassThru</span></span>
<span data-ttu-id="56164-116">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="56164-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="56164-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56164-117">-ResourceGroupName</span></span>
<span data-ttu-id="56164-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="56164-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="56164-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56164-119">-Confirm</span></span>
<span data-ttu-id="56164-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="56164-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="56164-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56164-121">-WhatIf</span></span>
<span data-ttu-id="56164-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="56164-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="56164-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56164-123">CommonParameters</span></span>
<span data-ttu-id="56164-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56164-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56164-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56164-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56164-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56164-126">INPUTS</span></span>

### <span data-ttu-id="56164-127">System. String</span><span class="sxs-lookup"><span data-stu-id="56164-127">System.String</span></span>

## <span data-ttu-id="56164-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56164-128">OUTPUTS</span></span>

### <span data-ttu-id="56164-129">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="56164-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="56164-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56164-130">NOTES</span></span>
<span data-ttu-id="56164-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="56164-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="56164-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56164-132">RELATED LINKS</span></span>

[<span data-ttu-id="56164-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="56164-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="56164-134">Felfüggesztés – AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="56164-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
