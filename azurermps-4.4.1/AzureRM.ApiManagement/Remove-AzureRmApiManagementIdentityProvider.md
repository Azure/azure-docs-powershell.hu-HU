---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493893"
---
# <span data-ttu-id="2c803-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c803-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2c803-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c803-102">SYNOPSIS</span></span>
<span data-ttu-id="2c803-103">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="2c803-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c803-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c803-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c803-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c803-105">DESCRIPTION</span></span>
<span data-ttu-id="2c803-106">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="2c803-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="2c803-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2c803-107">EXAMPLES</span></span>

### <span data-ttu-id="2c803-108">A Facebook-identitás-szolgáltató beállításainak eltávolítása a ApiManagement szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="2c803-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="2c803-109">A Facebook-identitás-szolgáltató konfigurációját érintő konfiguráció törlése.</span><span class="sxs-lookup"><span data-stu-id="2c803-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="2c803-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c803-110">PARAMETERS</span></span>

### <span data-ttu-id="2c803-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2c803-111">-Context</span></span>
<span data-ttu-id="2c803-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="2c803-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2c803-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2c803-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2c803-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c803-114">-PassThru</span></span>
<span data-ttu-id="2c803-115">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="2c803-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="2c803-116">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="2c803-116">-Type</span></span>
<span data-ttu-id="2c803-117">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c803-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="2c803-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2c803-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c803-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c803-119">-Confirm</span></span>
<span data-ttu-id="2c803-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c803-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c803-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c803-121">-WhatIf</span></span>
<span data-ttu-id="2c803-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c803-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c803-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c803-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c803-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c803-124">-DefaultProfile</span></span>
<span data-ttu-id="2c803-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c803-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c803-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c803-126">CommonParameters</span></span>
<span data-ttu-id="2c803-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c803-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c803-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c803-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c803-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c803-129">INPUTS</span></span>

## <span data-ttu-id="2c803-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c803-130">OUTPUTS</span></span>

### <span data-ttu-id="2c803-131">bool</span><span class="sxs-lookup"><span data-stu-id="2c803-131">bool</span></span>

## <span data-ttu-id="2c803-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c803-132">NOTES</span></span>

## <span data-ttu-id="2c803-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c803-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c803-134">Új – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c803-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="2c803-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c803-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="2c803-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c803-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

