---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018004"
---
# <span data-ttu-id="a3820-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="a3820-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="a3820-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3820-102">SYNOPSIS</span></span>
<span data-ttu-id="a3820-103">Egy felhasználó bejelentkezési URL-címét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a3820-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="a3820-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3820-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3820-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3820-105">DESCRIPTION</span></span>
<span data-ttu-id="a3820-106">A **Get-AzApiManagementUserSsoUrl** parancsmag egyszeri bejelentkezési (SSO) URL-címet hoz létre a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="a3820-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="a3820-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a3820-107">EXAMPLES</span></span>

### <span data-ttu-id="a3820-108">Példa 1: felhasználó bejelentkezési URL-címének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a3820-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="a3820-109">Ez a parancs a felhasználó bejelentkezési URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a3820-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="a3820-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3820-110">PARAMETERS</span></span>

### <span data-ttu-id="a3820-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a3820-111">-Context</span></span>
<span data-ttu-id="a3820-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a3820-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a3820-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a3820-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a3820-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3820-114">-DefaultProfile</span></span>
<span data-ttu-id="a3820-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3820-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3820-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="a3820-116">-UserId</span></span>
<span data-ttu-id="a3820-117">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a3820-117">Specifies a user ID.</span></span>
<span data-ttu-id="a3820-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a3820-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a3820-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3820-119">CommonParameters</span></span>
<span data-ttu-id="a3820-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3820-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3820-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3820-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3820-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3820-122">INPUTS</span></span>

### <span data-ttu-id="a3820-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a3820-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a3820-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a3820-124">System.String</span></span>

## <span data-ttu-id="a3820-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3820-125">OUTPUTS</span></span>

### <span data-ttu-id="a3820-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a3820-126">System.String</span></span>

## <span data-ttu-id="a3820-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3820-127">NOTES</span></span>

## <span data-ttu-id="a3820-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3820-128">RELATED LINKS</span></span>

[<span data-ttu-id="a3820-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a3820-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


