---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017978"
---
# <span data-ttu-id="a7160-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a7160-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a7160-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7160-102">SYNOPSIS</span></span>
<span data-ttu-id="a7160-103">Az alkalmazások folyamatos exportálási konfigurációjának beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="a7160-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a7160-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7160-104">SYNTAX</span></span>

### <span data-ttu-id="a7160-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7160-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7160-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7160-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7160-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7160-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7160-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7160-108">DESCRIPTION</span></span>
<span data-ttu-id="a7160-109">Az alkalmazások folyamatos exportálási konfigurációjának beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="a7160-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a7160-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a7160-110">EXAMPLES</span></span>

### <span data-ttu-id="a7160-111">Példa 1 a folyamatos exportálás beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="a7160-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="a7160-112">A "teszt" erőforráscsoport "testgroup" erőforráscsoport nevű erőforrás-konfigurációk folyamatos exportálási konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a7160-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="a7160-113">2 példa – folyamatos exportálás beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="a7160-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="a7160-114">Az alkalmazások folyamatos exportálási beállításainak beolvasása a "teszt" erőforráscsoport "testgroup" erőforráscsoporthoz tartozó "ZJrfffySPdtG3ESn3iRxVIEFuNY =" exportálási azonosítójú azonosítójú erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="a7160-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a7160-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7160-115">PARAMETERS</span></span>

### <span data-ttu-id="a7160-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a7160-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a7160-117">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="a7160-117">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7160-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7160-118">-DefaultProfile</span></span>
<span data-ttu-id="a7160-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7160-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7160-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="a7160-120">-ExportId</span></span>
<span data-ttu-id="a7160-121">Az alkalmazás betekintést nyújt a folyamatos exportálási azonosítóra.</span><span class="sxs-lookup"><span data-stu-id="a7160-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7160-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7160-122">-Name</span></span>
<span data-ttu-id="a7160-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="a7160-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7160-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7160-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7160-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a7160-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7160-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7160-126">-ResourceId</span></span>
<span data-ttu-id="a7160-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a7160-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7160-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7160-128">CommonParameters</span></span>
<span data-ttu-id="a7160-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7160-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7160-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7160-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7160-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7160-131">INPUTS</span></span>

### <span data-ttu-id="a7160-132">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a7160-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a7160-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a7160-133">System.String</span></span>

## <span data-ttu-id="a7160-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7160-134">OUTPUTS</span></span>

### <span data-ttu-id="a7160-135">Microsoft. Azure. Command. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7160-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="a7160-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7160-136">NOTES</span></span>

## <span data-ttu-id="a7160-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7160-137">RELATED LINKS</span></span>
