---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 5b8c781380ced5ed174c094cf1ff66a8eb820309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011921"
---
# <span data-ttu-id="556a1-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="556a1-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="556a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="556a1-102">SYNOPSIS</span></span>
<span data-ttu-id="556a1-103">Megosztott hozzáférési tokent hoz létre a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="556a1-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="556a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="556a1-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="556a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="556a1-105">DESCRIPTION</span></span>
<span data-ttu-id="556a1-106">A **New-AzApiManagementUserToken** parancsmag létrehoz egy megosztott hozzáférési jogkivonatot egy adott felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="556a1-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="556a1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="556a1-107">EXAMPLES</span></span>

### <span data-ttu-id="556a1-108">Példa 1: megosztott hozzáférési jogkivonat létrehozása a git-felhasználóknak</span><span class="sxs-lookup"><span data-stu-id="556a1-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="556a1-109">Ez a parancsfájl beolvassa a ApiManagement szolgáltatásban konfigurált git-felhasználót, és egy megosztott hozzáférési jogkivonatot hoz létre a 8 órára érvényes elsődleges kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="556a1-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="556a1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="556a1-110">PARAMETERS</span></span>

### <span data-ttu-id="556a1-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="556a1-111">-Context</span></span>
<span data-ttu-id="556a1-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="556a1-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="556a1-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="556a1-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="556a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556a1-114">-DefaultProfile</span></span>
<span data-ttu-id="556a1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="556a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="556a1-116">-Lejárat</span><span class="sxs-lookup"><span data-stu-id="556a1-116">-Expiry</span></span>
<span data-ttu-id="556a1-117">A jogkivonat lejárta</span><span class="sxs-lookup"><span data-stu-id="556a1-117">Expiry of the Token.</span></span>
<span data-ttu-id="556a1-118">Ha nincs megadva, a token 8 óra elteltével jön létre.</span><span class="sxs-lookup"><span data-stu-id="556a1-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="556a1-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="556a1-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="556a1-120">-Típus</span><span class="sxs-lookup"><span data-stu-id="556a1-120">-KeyType</span></span>
<span data-ttu-id="556a1-121">A jogkivonat generálásakor használandó felhasználói kulcs.</span><span class="sxs-lookup"><span data-stu-id="556a1-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="556a1-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="556a1-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="556a1-123">-UserId</span><span class="sxs-lookup"><span data-stu-id="556a1-123">-UserId</span></span>
<span data-ttu-id="556a1-124">A meglévő felhasználó azonosítója</span><span class="sxs-lookup"><span data-stu-id="556a1-124">Identifier of existing user.</span></span>
<span data-ttu-id="556a1-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="556a1-125">This parameter is required.</span></span>

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

### <span data-ttu-id="556a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556a1-126">CommonParameters</span></span>
<span data-ttu-id="556a1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="556a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556a1-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="556a1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556a1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="556a1-129">INPUTS</span></span>

### <span data-ttu-id="556a1-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="556a1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="556a1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="556a1-131">System.String</span></span>

### <span data-ttu-id="556a1-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="556a1-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="556a1-133">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="556a1-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="556a1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="556a1-134">OUTPUTS</span></span>

### <span data-ttu-id="556a1-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="556a1-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="556a1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="556a1-136">NOTES</span></span>

## <span data-ttu-id="556a1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="556a1-137">RELATED LINKS</span></span>
