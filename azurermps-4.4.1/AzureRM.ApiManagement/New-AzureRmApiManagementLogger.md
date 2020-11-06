---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: c7827f0df8b1baf4bb2fead9df091619751c969c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498044"
---
# <span data-ttu-id="d4057-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d4057-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="d4057-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4057-102">SYNOPSIS</span></span>
<span data-ttu-id="d4057-103">API-kezelési naplózó hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d4057-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4057-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4057-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4057-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4057-105">DESCRIPTION</span></span>
<span data-ttu-id="d4057-106">A **New-AzureRmApiManagementLogger** parancsmag egy Azure API-kezelési **naplózó** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d4057-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="d4057-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d4057-107">EXAMPLES</span></span>

### <span data-ttu-id="d4057-108">Példa 1: Tuskózó létrehozása</span><span class="sxs-lookup"><span data-stu-id="d4057-108">Example 1: Create a logger</span></span>
```
PS C:\>New-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="d4057-109">A parancs a megadott kapcsolati karakterlánccal létrehoz egy ContosoSdkEventHub nevű naplózó.</span><span class="sxs-lookup"><span data-stu-id="d4057-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="d4057-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4057-110">PARAMETERS</span></span>

### <span data-ttu-id="d4057-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d4057-111">-ConnectionString</span></span>
<span data-ttu-id="d4057-112">Az Azure Event hubok kapcsolati karakterláncát adja meg, amely a következővel kezdődik:</span><span class="sxs-lookup"><span data-stu-id="d4057-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="d4057-113">A kapcsolati karakterláncban a küldési jogosultságokat tartalmazó kulcsot be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="d4057-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="d4057-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d4057-114">-Context</span></span>
<span data-ttu-id="d4057-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d4057-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d4057-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d4057-116">-Description</span></span>
<span data-ttu-id="d4057-117">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="d4057-117">Specifies a description.</span></span>

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

### <span data-ttu-id="d4057-118">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="d4057-118">-IsBuffered</span></span>
<span data-ttu-id="d4057-119">Azt adja meg, hogy a naplózó rekordjai a közzététel előtt puffereltek-e.</span><span class="sxs-lookup"><span data-stu-id="d4057-119">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="d4057-120">Az alapértelmezett érték $True.</span><span class="sxs-lookup"><span data-stu-id="d4057-120">The default value is $True.</span></span>
<span data-ttu-id="d4057-121">Ha a rekordokat pufferelte, akkor a rendszer 15 másodpercenként elküldi az esemény-huboknak, vagy ha a puffer az 256 KB-ot kapja.</span><span class="sxs-lookup"><span data-stu-id="d4057-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4057-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d4057-122">-LoggerId</span></span>
<span data-ttu-id="d4057-123">A Logger AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4057-123">Specifies an ID for the logger.</span></span>
<span data-ttu-id="d4057-124">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="d4057-124">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="d4057-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4057-125">-Name</span></span>
<span data-ttu-id="d4057-126">Az Azure Classic portálról adja meg az esemény központja egyedének nevét.</span><span class="sxs-lookup"><span data-stu-id="d4057-126">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="d4057-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4057-127">-DefaultProfile</span></span>
<span data-ttu-id="d4057-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4057-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4057-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4057-129">CommonParameters</span></span>
<span data-ttu-id="d4057-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4057-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4057-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4057-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4057-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4057-132">INPUTS</span></span>

## <span data-ttu-id="d4057-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4057-133">OUTPUTS</span></span>

### <span data-ttu-id="d4057-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d4057-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="d4057-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4057-135">NOTES</span></span>

## <span data-ttu-id="d4057-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4057-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4057-137">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d4057-137">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d4057-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d4057-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d4057-139">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d4057-139">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


