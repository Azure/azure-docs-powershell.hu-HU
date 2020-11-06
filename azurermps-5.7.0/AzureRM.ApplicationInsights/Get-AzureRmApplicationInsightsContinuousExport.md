---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 5e3b2feff3b59df30960856718911a3aeb699c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499095"
---
# <span data-ttu-id="664ca-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="664ca-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="664ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="664ca-102">SYNOPSIS</span></span>
<span data-ttu-id="664ca-103">Az alkalmazások folyamatos exportálási konfigurációjának beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="664ca-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="664ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="664ca-104">SYNTAX</span></span>

### <span data-ttu-id="664ca-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="664ca-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="664ca-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="664ca-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="664ca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="664ca-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="664ca-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="664ca-108">DESCRIPTION</span></span>
<span data-ttu-id="664ca-109">Az alkalmazások folyamatos exportálási konfigurációjának beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="664ca-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="664ca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="664ca-110">EXAMPLES</span></span>

### <span data-ttu-id="664ca-111">Példa 1 a folyamatos exportálás beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="664ca-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="664ca-112">A "teszt" erőforráscsoport "testgroup" erőforráscsoport nevű erőforrás-konfigurációk folyamatos exportálási konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="664ca-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="664ca-113">2 példa – folyamatos exportálás beolvasása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="664ca-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="664ca-114">Az alkalmazások folyamatos exportálási beállításainak beolvasása a "teszt" erőforráscsoport "testgroup" erőforráscsoporthoz tartozó "ZJrfffySPdtG3ESn3iRxVIEFuNY =" exportálási azonosítójú azonosítójú erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="664ca-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="664ca-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="664ca-115">PARAMETERS</span></span>

### <span data-ttu-id="664ca-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="664ca-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="664ca-117">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="664ca-117">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="664ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664ca-118">-DefaultProfile</span></span>
<span data-ttu-id="664ca-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="664ca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="664ca-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="664ca-120">-ExportId</span></span>
<span data-ttu-id="664ca-121">Az alkalmazás betekintést nyújt a folyamatos exportálási azonosítóra.</span><span class="sxs-lookup"><span data-stu-id="664ca-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664ca-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="664ca-122">-Name</span></span>
<span data-ttu-id="664ca-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="664ca-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="664ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="664ca-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="664ca-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664ca-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="664ca-126">-ResourceId</span></span>
<span data-ttu-id="664ca-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="664ca-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664ca-128">CommonParameters</span></span>
<span data-ttu-id="664ca-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="664ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664ca-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664ca-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664ca-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="664ca-131">INPUTS</span></span>

### <span data-ttu-id="664ca-132">System. String</span><span class="sxs-lookup"><span data-stu-id="664ca-132">System.String</span></span>

## <span data-ttu-id="664ca-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="664ca-133">OUTPUTS</span></span>

### <span data-ttu-id="664ca-134">Microsoft. Azure. Command. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="664ca-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="664ca-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="664ca-135">NOTES</span></span>

## <span data-ttu-id="664ca-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="664ca-136">RELATED LINKS</span></span>

