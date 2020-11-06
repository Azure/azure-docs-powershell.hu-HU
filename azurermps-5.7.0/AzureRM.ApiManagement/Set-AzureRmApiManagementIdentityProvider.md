---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e45ec5a3d49bf82ab945a3ef3b41362a1e1e2bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504616"
---
# <span data-ttu-id="ec46d-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec46d-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ec46d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec46d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec46d-103">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ec46d-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec46d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec46d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec46d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec46d-105">DESCRIPTION</span></span>
<span data-ttu-id="ec46d-106">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ec46d-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="ec46d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec46d-107">EXAMPLES</span></span>

### <span data-ttu-id="ec46d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec46d-108">Example 1</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="ec46d-109">A parancsmag frissíti a Facebook-identitás szolgáltatójának az ügyfél titkát;</span><span class="sxs-lookup"><span data-stu-id="ec46d-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="ec46d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec46d-110">PARAMETERS</span></span>

### <span data-ttu-id="ec46d-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="ec46d-111">-AllowedTenants</span></span>
<span data-ttu-id="ec46d-112">Az engedélyezett Azure Active Directory-bérlők listája.</span><span class="sxs-lookup"><span data-stu-id="ec46d-112">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec46d-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="ec46d-113">-ClientId</span></span>
<span data-ttu-id="ec46d-114">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="ec46d-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="ec46d-115">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ec46d-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec46d-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ec46d-116">-ClientSecret</span></span>
<span data-ttu-id="ec46d-117">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ec46d-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="ec46d-118">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="ec46d-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec46d-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ec46d-119">-Context</span></span>
<span data-ttu-id="ec46d-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ec46d-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ec46d-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ec46d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="ec46d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec46d-122">-DefaultProfile</span></span>
<span data-ttu-id="ec46d-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec46d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ec46d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec46d-124">-PassThru</span></span>
<span data-ttu-id="ec46d-125">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementIdentityProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ec46d-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec46d-126">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ec46d-126">-Type</span></span>
<span data-ttu-id="ec46d-127">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec46d-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="ec46d-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ec46d-128">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec46d-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec46d-129">-Confirm</span></span>
<span data-ttu-id="ec46d-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec46d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec46d-131">-WhatIf</span></span>
<span data-ttu-id="ec46d-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec46d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec46d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec46d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec46d-134">CommonParameters</span></span>
<span data-ttu-id="ec46d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec46d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec46d-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec46d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec46d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec46d-137">INPUTS</span></span>

### <span data-ttu-id="ec46d-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="ec46d-138">None</span></span>
<span data-ttu-id="ec46d-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ec46d-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec46d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec46d-140">OUTPUTS</span></span>

### <span data-ttu-id="ec46d-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec46d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ec46d-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec46d-142">NOTES</span></span>

## <span data-ttu-id="ec46d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec46d-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec46d-144">Új – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec46d-144">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="ec46d-145">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec46d-145">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="ec46d-146">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec46d-146">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
