---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: 3df5f6974cd955035c16972a5a7358aa44a30390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671670"
---
# <span data-ttu-id="66d72-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66d72-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="66d72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66d72-102">SYNOPSIS</span></span>
<span data-ttu-id="66d72-103">API-kezelési naplózó hoz létre.</span><span class="sxs-lookup"><span data-stu-id="66d72-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="66d72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66d72-104">SYNTAX</span></span>

### <span data-ttu-id="66d72-105">EventHubLoggerSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66d72-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d72-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="66d72-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66d72-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="66d72-107">DESCRIPTION</span></span>
<span data-ttu-id="66d72-108">A **New-AzApiManagementLogger** parancsmag egy Azure API-kezelési **naplózó** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="66d72-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="66d72-109">Példák</span><span class="sxs-lookup"><span data-stu-id="66d72-109">EXAMPLES</span></span>

### <span data-ttu-id="66d72-110">Példa 1: Tuskózó létrehozása</span><span class="sxs-lookup"><span data-stu-id="66d72-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="66d72-111">A parancs a megadott kapcsolati karakterlánccal létrehoz egy ContosoSdkEventHub nevű naplózó.</span><span class="sxs-lookup"><span data-stu-id="66d72-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="66d72-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66d72-112">PARAMETERS</span></span>

### <span data-ttu-id="66d72-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="66d72-113">-ConnectionString</span></span>
<span data-ttu-id="66d72-114">Az Azure Event hubok kapcsolati karakterláncát adja meg, amely a következővel kezdődik: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="66d72-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="66d72-115">A kapcsolati karakterláncban a küldési jogosultságokat tartalmazó kulcsot be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="66d72-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d72-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="66d72-116">-Context</span></span>
<span data-ttu-id="66d72-117">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="66d72-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="66d72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d72-118">-DefaultProfile</span></span>
<span data-ttu-id="66d72-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66d72-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66d72-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="66d72-120">-Description</span></span>
<span data-ttu-id="66d72-121">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="66d72-121">Specifies a description.</span></span>

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

### <span data-ttu-id="66d72-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="66d72-122">-InstrumentationKey</span></span>
<span data-ttu-id="66d72-123">Az alkalmazási áttekintések Instrumentation kulcsa.</span><span class="sxs-lookup"><span data-stu-id="66d72-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="66d72-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="66d72-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d72-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="66d72-125">-IsBuffered</span></span>
<span data-ttu-id="66d72-126">Azt adja meg, hogy a naplózó rekordjai a közzététel előtt puffereltek-e.</span><span class="sxs-lookup"><span data-stu-id="66d72-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="66d72-127">Az alapértelmezett érték $True.</span><span class="sxs-lookup"><span data-stu-id="66d72-127">The default value is $True.</span></span>
<span data-ttu-id="66d72-128">Ha a rekordokat pufferelte, akkor a rendszer 15 másodpercenként elküldi az esemény-huboknak, vagy ha a puffer az 256 KB-ot kapja.</span><span class="sxs-lookup"><span data-stu-id="66d72-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d72-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="66d72-129">-LoggerId</span></span>
<span data-ttu-id="66d72-130">A Logger AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="66d72-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="66d72-131">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="66d72-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="66d72-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66d72-132">-Name</span></span>
<span data-ttu-id="66d72-133">Az Azure Classic portálról adja meg az esemény központja egyedének nevét.</span><span class="sxs-lookup"><span data-stu-id="66d72-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d72-134">CommonParameters</span></span>
<span data-ttu-id="66d72-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66d72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d72-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d72-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d72-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d72-137">INPUTS</span></span>

### <span data-ttu-id="66d72-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66d72-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66d72-139">System. String</span><span class="sxs-lookup"><span data-stu-id="66d72-139">System.String</span></span>

### <span data-ttu-id="66d72-140">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66d72-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="66d72-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d72-141">OUTPUTS</span></span>

### <span data-ttu-id="66d72-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66d72-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="66d72-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66d72-143">NOTES</span></span>

## <span data-ttu-id="66d72-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66d72-144">RELATED LINKS</span></span>

[<span data-ttu-id="66d72-145">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66d72-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="66d72-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66d72-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="66d72-147">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66d72-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


