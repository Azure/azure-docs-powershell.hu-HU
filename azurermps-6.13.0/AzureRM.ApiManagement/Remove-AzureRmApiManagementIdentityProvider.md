---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492061"
---
# <span data-ttu-id="bc54b-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bc54b-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="bc54b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc54b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc54b-103">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="bc54b-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc54b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc54b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc54b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc54b-105">DESCRIPTION</span></span>
<span data-ttu-id="bc54b-106">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="bc54b-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="bc54b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc54b-107">EXAMPLES</span></span>

### <span data-ttu-id="bc54b-108">A Facebook-identitás-szolgáltató beállításainak eltávolítása a ApiManagement szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="bc54b-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="bc54b-109">A Facebook-identitás-szolgáltató konfigurációját érintő konfiguráció törlése.</span><span class="sxs-lookup"><span data-stu-id="bc54b-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="bc54b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc54b-110">PARAMETERS</span></span>

### <span data-ttu-id="bc54b-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bc54b-111">-Context</span></span>
<span data-ttu-id="bc54b-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="bc54b-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bc54b-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bc54b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="bc54b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc54b-114">-DefaultProfile</span></span>
<span data-ttu-id="bc54b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc54b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc54b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc54b-116">-PassThru</span></span>
<span data-ttu-id="bc54b-117">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="bc54b-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="bc54b-118">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="bc54b-118">-Type</span></span>
<span data-ttu-id="bc54b-119">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bc54b-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="bc54b-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bc54b-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc54b-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc54b-121">-Confirm</span></span>
<span data-ttu-id="bc54b-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc54b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc54b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc54b-123">-WhatIf</span></span>
<span data-ttu-id="bc54b-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc54b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc54b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc54b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc54b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc54b-126">CommonParameters</span></span>
<span data-ttu-id="bc54b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc54b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc54b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc54b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc54b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc54b-129">INPUTS</span></span>

### <span data-ttu-id="bc54b-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc54b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc54b-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="bc54b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="bc54b-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc54b-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc54b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc54b-133">OUTPUTS</span></span>

### <span data-ttu-id="bc54b-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc54b-134">System.Boolean</span></span>

## <span data-ttu-id="bc54b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc54b-135">NOTES</span></span>

## <span data-ttu-id="bc54b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc54b-136">RELATED LINKS</span></span>

[<span data-ttu-id="bc54b-137">Új – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bc54b-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="bc54b-138">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bc54b-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="bc54b-139">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bc54b-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

