---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 651ef4c0c44b7e3269eb300dcfa098c39415f77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678998"
---
# <span data-ttu-id="df715-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df715-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="df715-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df715-102">SYNOPSIS</span></span>
<span data-ttu-id="df715-103">API-kezelési engedélyezési kiszolgáló kapja.</span><span class="sxs-lookup"><span data-stu-id="df715-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df715-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df715-104">SYNTAX</span></span>

### <span data-ttu-id="df715-105">GetAllAuthorizationServers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df715-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df715-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="df715-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df715-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df715-107">DESCRIPTION</span></span>
<span data-ttu-id="df715-108">A **Get-AzureRmApiManagementAuthorizationServer** parancsmag minden Azure API-kezelési engedélyezési kiszolgálót vagy megadott engedélyezési kiszolgálót kap.</span><span class="sxs-lookup"><span data-stu-id="df715-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="df715-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df715-109">EXAMPLES</span></span>

### <span data-ttu-id="df715-110">1. példa: az összes engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="df715-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="df715-111">Ez a parancs minden API-kezelési engedélyezési kiszolgálót beolvassa.</span><span class="sxs-lookup"><span data-stu-id="df715-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="df715-112">2. példa: meghatározott engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="df715-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="df715-113">Ez a parancs a megadott engedélyezési kiszolgálót kapja.</span><span class="sxs-lookup"><span data-stu-id="df715-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="df715-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df715-114">PARAMETERS</span></span>

### <span data-ttu-id="df715-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="df715-115">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df715-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df715-116">-DefaultProfile</span></span>
<span data-ttu-id="df715-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df715-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="df715-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="df715-118">-ServerId</span></span>
```yaml
Type: String
Parameter Sets: GetByServerId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df715-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df715-119">CommonParameters</span></span>
<span data-ttu-id="df715-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df715-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df715-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df715-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df715-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df715-122">INPUTS</span></span>

### <span data-ttu-id="df715-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="df715-123">None</span></span>
<span data-ttu-id="df715-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="df715-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df715-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df715-125">OUTPUTS</span></span>

### <span data-ttu-id="df715-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="df715-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>
<span data-ttu-id="df715-127">Az adott API-kezelési szolgáltatás engedélyezési kiszolgálójának adatai.</span><span class="sxs-lookup"><span data-stu-id="df715-127">The details of the Authorization Server in a given Api Management service.</span></span>

### <span data-ttu-id="df715-128">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="df715-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>
<span data-ttu-id="df715-129">Az adott API-kezelési szolgáltatás engedélyezési kiszolgálójának listája.</span><span class="sxs-lookup"><span data-stu-id="df715-129">The list of Authorization Server in a given Api Management service.</span></span>

## <span data-ttu-id="df715-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df715-130">NOTES</span></span>

## <span data-ttu-id="df715-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df715-131">RELATED LINKS</span></span>

[<span data-ttu-id="df715-132">Új – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df715-132">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="df715-133">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df715-133">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="df715-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df715-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


