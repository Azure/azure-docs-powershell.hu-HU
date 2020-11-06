---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495187"
---
# <span data-ttu-id="0bb4e-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0bb4e-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="0bb4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0bb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb4e-103">API-kezelési naplózó módosítása</span><span class="sxs-lookup"><span data-stu-id="0bb4e-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0bb4e-104">SYNTAX</span></span>

### <span data-ttu-id="0bb4e-105">EventHubLoggerSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0bb4e-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bb4e-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="0bb4e-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bb4e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0bb4e-107">DESCRIPTION</span></span>
<span data-ttu-id="0bb4e-108">A **set-AzureRmApiManagementLogger** parancsmag módosította az Azure API-kezelési **naplózó** beállításait.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="0bb4e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0bb4e-109">EXAMPLES</span></span>

### <span data-ttu-id="0bb4e-110">Példa 1: a EventHub Logger módosítása</span><span class="sxs-lookup"><span data-stu-id="0bb4e-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="0bb4e-111">Ez a parancs módosítja az id Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="0bb4e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0bb4e-112">PARAMETERS</span></span>

### <span data-ttu-id="0bb4e-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0bb4e-113">-ConnectionString</span></span>
<span data-ttu-id="0bb4e-114">Egy Azure-esemény hubok kapcsolati karakterláncát adja meg, amely a házirend-jogosultságok küldését is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb4e-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0bb4e-115">-Context</span></span>
<span data-ttu-id="0bb4e-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb4e-117">-DefaultProfile</span></span>
<span data-ttu-id="0bb4e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb4e-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0bb4e-119">-Description</span></span>
<span data-ttu-id="0bb4e-120">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-120">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb4e-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="0bb4e-121">-InstrumentationKey</span></span>
<span data-ttu-id="0bb4e-122">Az alkalmazási áttekintések Instrumentation kulcsa.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="0bb4e-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb4e-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="0bb4e-124">-IsBuffered</span></span>
<span data-ttu-id="0bb4e-125">Azt adja meg, hogy a naplózó rekordjai a közzététel előtt puffereltek.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="0bb4e-126">Ha a rekordokat pufferelte, akkor a rendszer 15 másodpercenként elküldi az esemény-huboknak, vagy ha a puffer az 256 KB-ot kapja.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb4e-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="0bb4e-127">-LoggerId</span></span>
<span data-ttu-id="0bb4e-128">A frissítendő naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-128">Specifies the ID of the logger to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb4e-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0bb4e-129">-Name</span></span>
<span data-ttu-id="0bb4e-130">Az Azure Classic portálról adja meg az esemény központja egyedének nevét.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb4e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bb4e-131">-PassThru</span></span>
<span data-ttu-id="0bb4e-132">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementLogger** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0bb4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb4e-133">CommonParameters</span></span>
<span data-ttu-id="0bb4e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0bb4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb4e-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb4e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb4e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bb4e-136">INPUTS</span></span>

### <span data-ttu-id="0bb4e-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0bb4e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0bb4e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0bb4e-138">System.String</span></span>

### <span data-ttu-id="0bb4e-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0bb4e-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0bb4e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bb4e-140">OUTPUTS</span></span>

### <span data-ttu-id="0bb4e-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0bb4e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="0bb4e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0bb4e-142">NOTES</span></span>

## <span data-ttu-id="0bb4e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bb4e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0bb4e-144">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0bb4e-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0bb4e-145">Új – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0bb4e-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0bb4e-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0bb4e-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


