---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836910"
---
# <span data-ttu-id="c7916-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7916-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="c7916-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7916-102">SYNOPSIS</span></span>
<span data-ttu-id="c7916-103">API-kezelési naplózó módosítása</span><span class="sxs-lookup"><span data-stu-id="c7916-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="c7916-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7916-104">SYNTAX</span></span>

### <span data-ttu-id="c7916-105">EventHubLoggerSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7916-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7916-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="c7916-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7916-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7916-107">DESCRIPTION</span></span>
<span data-ttu-id="c7916-108">A **set-AzApiManagementLogger** parancsmag módosította az Azure API-kezelési **naplózó** beállításait.</span><span class="sxs-lookup"><span data-stu-id="c7916-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="c7916-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c7916-109">EXAMPLES</span></span>

### <span data-ttu-id="c7916-110">Példa 1: a EventHub Logger módosítása</span><span class="sxs-lookup"><span data-stu-id="c7916-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="c7916-111">Ez a parancs módosítja az id Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="c7916-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="c7916-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7916-112">PARAMETERS</span></span>

### <span data-ttu-id="c7916-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c7916-113">-ConnectionString</span></span>
<span data-ttu-id="c7916-114">Egy Azure-esemény hubok kapcsolati karakterláncát adja meg, amely a házirend-jogosultságok küldését is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c7916-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="c7916-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c7916-115">-Context</span></span>
<span data-ttu-id="c7916-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c7916-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c7916-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7916-117">-DefaultProfile</span></span>
<span data-ttu-id="c7916-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7916-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7916-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c7916-119">-Description</span></span>
<span data-ttu-id="c7916-120">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="c7916-120">Specifies a description.</span></span>

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

### <span data-ttu-id="c7916-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="c7916-121">-InstrumentationKey</span></span>
<span data-ttu-id="c7916-122">Az alkalmazási áttekintések Instrumentation kulcsa.</span><span class="sxs-lookup"><span data-stu-id="c7916-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="c7916-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c7916-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7916-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="c7916-124">-IsBuffered</span></span>
<span data-ttu-id="c7916-125">Azt adja meg, hogy a naplózó rekordjai a közzététel előtt puffereltek.</span><span class="sxs-lookup"><span data-stu-id="c7916-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="c7916-126">Ha a rekordokat pufferelte, akkor a rendszer 15 másodpercenként elküldi az esemény-huboknak, vagy ha a puffer az 256 KB-ot kapja.</span><span class="sxs-lookup"><span data-stu-id="c7916-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="c7916-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c7916-127">-LoggerId</span></span>
<span data-ttu-id="c7916-128">A frissítendő naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7916-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="c7916-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7916-129">-Name</span></span>
<span data-ttu-id="c7916-130">Az Azure Classic portálról adja meg az esemény központja egyedének nevét.</span><span class="sxs-lookup"><span data-stu-id="c7916-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="c7916-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7916-131">-PassThru</span></span>
<span data-ttu-id="c7916-132">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementLogger** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c7916-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c7916-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7916-133">CommonParameters</span></span>
<span data-ttu-id="c7916-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7916-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7916-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7916-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7916-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7916-136">INPUTS</span></span>

### <span data-ttu-id="c7916-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7916-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7916-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c7916-138">System.String</span></span>

### <span data-ttu-id="c7916-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7916-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7916-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7916-140">OUTPUTS</span></span>

### <span data-ttu-id="c7916-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7916-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c7916-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7916-142">NOTES</span></span>

## <span data-ttu-id="c7916-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7916-143">RELATED LINKS</span></span>

[<span data-ttu-id="c7916-144">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7916-144">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="c7916-145">Új – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7916-145">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="c7916-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7916-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


