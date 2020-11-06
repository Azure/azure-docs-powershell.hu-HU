---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 92e241703723d055d18083daae5fe424933f7c3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503900"
---
# <span data-ttu-id="fcf31-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fcf31-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fcf31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcf31-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf31-103">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="fcf31-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcf31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcf31-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcf31-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf31-106">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="fcf31-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="fcf31-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fcf31-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf31-108">A Facebook-identitás-szolgáltató beállításainak eltávolítása a ApiManagement szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="fcf31-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="fcf31-109">A Facebook-identitás-szolgáltató konfigurációját érintő konfiguráció törlése.</span><span class="sxs-lookup"><span data-stu-id="fcf31-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="fcf31-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcf31-110">PARAMETERS</span></span>

### <span data-ttu-id="fcf31-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fcf31-111">-Context</span></span>
<span data-ttu-id="fcf31-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="fcf31-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fcf31-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fcf31-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fcf31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf31-114">-DefaultProfile</span></span>
<span data-ttu-id="fcf31-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcf31-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fcf31-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcf31-116">-PassThru</span></span>
<span data-ttu-id="fcf31-117">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="fcf31-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="fcf31-118">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="fcf31-118">-Type</span></span>
<span data-ttu-id="fcf31-119">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fcf31-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="fcf31-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fcf31-120">This parameter is required.</span></span>

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

### <span data-ttu-id="fcf31-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fcf31-121">-Confirm</span></span>
<span data-ttu-id="fcf31-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcf31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf31-123">-WhatIf</span></span>
<span data-ttu-id="fcf31-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fcf31-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcf31-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcf31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf31-126">CommonParameters</span></span>
<span data-ttu-id="fcf31-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcf31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf31-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf31-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf31-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcf31-129">INPUTS</span></span>

### <span data-ttu-id="fcf31-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="fcf31-130">None</span></span>
<span data-ttu-id="fcf31-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fcf31-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcf31-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcf31-132">OUTPUTS</span></span>

### <span data-ttu-id="fcf31-133">bool</span><span class="sxs-lookup"><span data-stu-id="fcf31-133">bool</span></span>

## <span data-ttu-id="fcf31-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcf31-134">NOTES</span></span>

## <span data-ttu-id="fcf31-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcf31-135">RELATED LINKS</span></span>

[<span data-ttu-id="fcf31-136">Új – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fcf31-136">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="fcf31-137">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fcf31-137">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="fcf31-138">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fcf31-138">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

