---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 4453b7fc3e13f4de2632c41cea966fdada1d84f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504636"
---
# <span data-ttu-id="731b3-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="731b3-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="731b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="731b3-102">SYNOPSIS</span></span>
<span data-ttu-id="731b3-103">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="731b3-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="731b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="731b3-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="731b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="731b3-105">DESCRIPTION</span></span>
<span data-ttu-id="731b3-106">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="731b3-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="731b3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="731b3-107">EXAMPLES</span></span>

### <span data-ttu-id="731b3-108">Backend-hitelesítő adatok In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="731b3-108">Create a Backend Credentials In-Memory Object</span></span>
```
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="731b3-109">A backend-hitelesítő adatokkal rendelkező szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="731b3-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="731b3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="731b3-110">PARAMETERS</span></span>

### <span data-ttu-id="731b3-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="731b3-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="731b3-112">A backendhez használt engedélyezési fejléc.</span><span class="sxs-lookup"><span data-stu-id="731b3-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="731b3-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="731b3-113">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731b3-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="731b3-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="731b3-115">A backendhez használt engedélyezési séma.</span><span class="sxs-lookup"><span data-stu-id="731b3-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="731b3-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="731b3-116">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731b3-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="731b3-117">-CertificateThumbprint</span></span>
<span data-ttu-id="731b3-118">Ügyféltanúsítvány-Thumbprints</span><span class="sxs-lookup"><span data-stu-id="731b3-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="731b3-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="731b3-119">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731b3-120">-DefaultProfile</span></span>
<span data-ttu-id="731b3-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="731b3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="731b3-122">-Header</span><span class="sxs-lookup"><span data-stu-id="731b3-122">-Header</span></span>
<span data-ttu-id="731b3-123">A backend által elfogadott fejléc paraméter-értékek</span><span class="sxs-lookup"><span data-stu-id="731b3-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="731b3-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="731b3-124">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731b3-125">-Query</span><span class="sxs-lookup"><span data-stu-id="731b3-125">-Query</span></span>
<span data-ttu-id="731b3-126">A lekérdezés paramétereit a backend által elfogadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="731b3-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="731b3-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="731b3-127">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731b3-128">CommonParameters</span></span>
<span data-ttu-id="731b3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="731b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731b3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731b3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731b3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="731b3-131">INPUTS</span></span>

### <span data-ttu-id="731b3-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="731b3-132">None</span></span>
<span data-ttu-id="731b3-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="731b3-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="731b3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="731b3-134">OUTPUTS</span></span>

### <span data-ttu-id="731b3-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="731b3-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="731b3-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="731b3-136">NOTES</span></span>

## <span data-ttu-id="731b3-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="731b3-137">RELATED LINKS</span></span>

[<span data-ttu-id="731b3-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="731b3-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="731b3-139">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="731b3-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="731b3-140">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="731b3-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="731b3-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="731b3-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="731b3-142">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="731b3-142">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
