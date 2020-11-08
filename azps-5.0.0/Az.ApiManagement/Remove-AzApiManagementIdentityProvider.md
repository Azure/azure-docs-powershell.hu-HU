---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188149"
---
# <span data-ttu-id="e41f6-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e41f6-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e41f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e41f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e41f6-103">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e41f6-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="e41f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e41f6-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e41f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e41f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e41f6-106">Eltávolít egy meglévő személyazonosság-szolgáltatói konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e41f6-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="e41f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e41f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e41f6-108">Példa 1: a Facebook-identitás-szolgáltató beállításainak eltávolítása a ApiManagement szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="e41f6-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="e41f6-109">A Facebook-identitás-szolgáltató konfigurációját érintő konfiguráció törlése.</span><span class="sxs-lookup"><span data-stu-id="e41f6-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="e41f6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e41f6-110">PARAMETERS</span></span>

### <span data-ttu-id="e41f6-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e41f6-111">-Context</span></span>
<span data-ttu-id="e41f6-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="e41f6-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e41f6-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e41f6-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e41f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e41f6-114">-DefaultProfile</span></span>
<span data-ttu-id="e41f6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e41f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e41f6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e41f6-116">-PassThru</span></span>
<span data-ttu-id="e41f6-117">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="e41f6-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="e41f6-118">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e41f6-118">-Type</span></span>
<span data-ttu-id="e41f6-119">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e41f6-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="e41f6-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e41f6-120">This parameter is required.</span></span>

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

### <span data-ttu-id="e41f6-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e41f6-121">-Confirm</span></span>
<span data-ttu-id="e41f6-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e41f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e41f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e41f6-123">-WhatIf</span></span>
<span data-ttu-id="e41f6-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e41f6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e41f6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e41f6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e41f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e41f6-126">CommonParameters</span></span>
<span data-ttu-id="e41f6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e41f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e41f6-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e41f6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e41f6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e41f6-129">INPUTS</span></span>

### <span data-ttu-id="e41f6-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e41f6-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e41f6-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="e41f6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="e41f6-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e41f6-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e41f6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e41f6-133">OUTPUTS</span></span>

### <span data-ttu-id="e41f6-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e41f6-134">System.Boolean</span></span>

## <span data-ttu-id="e41f6-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e41f6-135">NOTES</span></span>

## <span data-ttu-id="e41f6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e41f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="e41f6-137">Új – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e41f6-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="e41f6-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e41f6-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="e41f6-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e41f6-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

