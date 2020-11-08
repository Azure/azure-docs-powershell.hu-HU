---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025602"
---
# <span data-ttu-id="fe537-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="fe537-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="fe537-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe537-102">SYNOPSIS</span></span>
<span data-ttu-id="fe537-103">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="fe537-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="fe537-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe537-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe537-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe537-105">DESCRIPTION</span></span>
<span data-ttu-id="fe537-106">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="fe537-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="fe537-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fe537-107">EXAMPLES</span></span>

### <span data-ttu-id="fe537-108">Példa 1: backend-hitelesítő adatok létrehozása In-Memory objektummal</span><span class="sxs-lookup"><span data-stu-id="fe537-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="fe537-109">A backend-hitelesítő adatokkal rendelkező szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe537-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="fe537-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe537-110">PARAMETERS</span></span>

### <span data-ttu-id="fe537-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="fe537-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="fe537-112">A backendhez használt engedélyezési fejléc.</span><span class="sxs-lookup"><span data-stu-id="fe537-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="fe537-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe537-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe537-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="fe537-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="fe537-115">A backendhez használt engedélyezési séma.</span><span class="sxs-lookup"><span data-stu-id="fe537-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="fe537-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe537-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe537-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="fe537-117">-CertificateThumbprint</span></span>
<span data-ttu-id="fe537-118">Ügyféltanúsítvány-Thumbprints</span><span class="sxs-lookup"><span data-stu-id="fe537-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="fe537-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe537-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe537-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe537-120">-DefaultProfile</span></span>
<span data-ttu-id="fe537-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe537-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe537-122">-Header</span><span class="sxs-lookup"><span data-stu-id="fe537-122">-Header</span></span>
<span data-ttu-id="fe537-123">A backend által elfogadott fejléc paraméter-értékek</span><span class="sxs-lookup"><span data-stu-id="fe537-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="fe537-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe537-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe537-125">-Query</span><span class="sxs-lookup"><span data-stu-id="fe537-125">-Query</span></span>
<span data-ttu-id="fe537-126">A lekérdezés paramétereit a backend által elfogadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="fe537-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="fe537-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe537-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe537-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe537-128">CommonParameters</span></span>
<span data-ttu-id="fe537-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe537-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe537-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe537-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe537-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe537-131">INPUTS</span></span>

### <span data-ttu-id="fe537-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe537-132">None</span></span>

## <span data-ttu-id="fe537-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe537-133">OUTPUTS</span></span>

### <span data-ttu-id="fe537-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="fe537-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="fe537-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe537-135">NOTES</span></span>

## <span data-ttu-id="fe537-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe537-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe537-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fe537-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="fe537-138">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fe537-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="fe537-139">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="fe537-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="fe537-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fe537-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="fe537-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fe537-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
