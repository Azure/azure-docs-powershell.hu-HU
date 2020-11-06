---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499291"
---
# <span data-ttu-id="19927-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19927-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="19927-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19927-102">SYNOPSIS</span></span>
<span data-ttu-id="19927-103">API-kezelési engedélyezési kiszolgáló kapja.</span><span class="sxs-lookup"><span data-stu-id="19927-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19927-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19927-104">SYNTAX</span></span>

### <span data-ttu-id="19927-105">Az összes engedélyezési kiszolgáló beszerzése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19927-105">Get all authorization server (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19927-106">Beolvasás azonosítóval</span><span class="sxs-lookup"><span data-stu-id="19927-106">Get by Id</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19927-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19927-107">DESCRIPTION</span></span>
<span data-ttu-id="19927-108">A **Get-AzureRmApiManagementAuthorizationServer** parancsmag minden Azure API-kezelési engedélyezési kiszolgálót vagy megadott engedélyezési kiszolgálót kap.</span><span class="sxs-lookup"><span data-stu-id="19927-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="19927-109">Példák</span><span class="sxs-lookup"><span data-stu-id="19927-109">EXAMPLES</span></span>

### <span data-ttu-id="19927-110">1. példa: az összes engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="19927-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="19927-111">Ez a parancs minden API-kezelési engedélyezési kiszolgálót beolvassa.</span><span class="sxs-lookup"><span data-stu-id="19927-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="19927-112">2. példa: meghatározott engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="19927-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="19927-113">Ez a parancs a megadott engedélyezési kiszolgálót kapja.</span><span class="sxs-lookup"><span data-stu-id="19927-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="19927-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19927-114">PARAMETERS</span></span>

### <span data-ttu-id="19927-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="19927-115">-Context</span></span>
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

### <span data-ttu-id="19927-116">-ServerId</span><span class="sxs-lookup"><span data-stu-id="19927-116">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19927-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19927-117">-DefaultProfile</span></span>
<span data-ttu-id="19927-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19927-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19927-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19927-119">CommonParameters</span></span>
<span data-ttu-id="19927-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19927-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19927-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19927-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19927-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19927-122">INPUTS</span></span>

## <span data-ttu-id="19927-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19927-123">OUTPUTS</span></span>

### <span data-ttu-id="19927-124">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="19927-124">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>

## <span data-ttu-id="19927-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19927-125">NOTES</span></span>

## <span data-ttu-id="19927-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19927-126">RELATED LINKS</span></span>

[<span data-ttu-id="19927-127">Új – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19927-127">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="19927-128">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19927-128">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="19927-129">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19927-129">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


