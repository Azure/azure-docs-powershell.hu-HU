---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0fc666ef1b747c7c114de560d241bcc2ac7be1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679227"
---
# <span data-ttu-id="917cf-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="917cf-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="917cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="917cf-102">SYNOPSIS</span></span>
<span data-ttu-id="917cf-103">Az Analysis Services Server példányának felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="917cf-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="917cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="917cf-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="917cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="917cf-105">DESCRIPTION</span></span>
<span data-ttu-id="917cf-106">Az Suspend-AzureRmAnalysisServicesServer parancsmag felfüggeszti az Analysis Services-kiszolgáló egy példányát.</span><span class="sxs-lookup"><span data-stu-id="917cf-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="917cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="917cf-107">EXAMPLES</span></span>

### <span data-ttu-id="917cf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="917cf-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="917cf-109">Ez a parancs felfüggeszti a TestServer nevű aktív kiszolgálót a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="917cf-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="917cf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="917cf-110">PARAMETERS</span></span>

### <span data-ttu-id="917cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917cf-111">-DefaultProfile</span></span>
<span data-ttu-id="917cf-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="917cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="917cf-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="917cf-113">-Name</span></span>
<span data-ttu-id="917cf-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="917cf-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="917cf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="917cf-115">-PassThru</span></span>
<span data-ttu-id="917cf-116">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="917cf-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="917cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="917cf-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="917cf-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="917cf-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="917cf-119">-Confirm</span></span>
<span data-ttu-id="917cf-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="917cf-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="917cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="917cf-121">-WhatIf</span></span>
<span data-ttu-id="917cf-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="917cf-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="917cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917cf-123">CommonParameters</span></span>
<span data-ttu-id="917cf-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="917cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917cf-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917cf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917cf-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="917cf-126">INPUTS</span></span>

### <span data-ttu-id="917cf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="917cf-127">System.String</span></span>

## <span data-ttu-id="917cf-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="917cf-128">OUTPUTS</span></span>

### <span data-ttu-id="917cf-129">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="917cf-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="917cf-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="917cf-130">NOTES</span></span>
<span data-ttu-id="917cf-131">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="917cf-131">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="917cf-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="917cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="917cf-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="917cf-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="917cf-134">Önéletrajz – AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="917cf-134">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

