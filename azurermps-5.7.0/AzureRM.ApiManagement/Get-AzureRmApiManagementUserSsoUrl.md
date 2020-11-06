---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 5cc7eb81c9ccaf461b1f2ab16e76aa662ea0f57b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495488"
---
# <span data-ttu-id="794f1-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="794f1-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="794f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="794f1-102">SYNOPSIS</span></span>
<span data-ttu-id="794f1-103">Egy felhasználó bejelentkezési URL-címét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="794f1-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="794f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="794f1-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="794f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="794f1-105">DESCRIPTION</span></span>
<span data-ttu-id="794f1-106">A **Get-AzureRmApiManagementUserSsoUrl** parancsmag egyszeri bejelentkezési (SSO) URL-címet hoz létre a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="794f1-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="794f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="794f1-107">EXAMPLES</span></span>

### <span data-ttu-id="794f1-108">Példa 1: felhasználó bejelentkezési URL-címének beszerzése</span><span class="sxs-lookup"><span data-stu-id="794f1-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="794f1-109">Ez a parancs a felhasználó bejelentkezési URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="794f1-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="794f1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="794f1-110">PARAMETERS</span></span>

### <span data-ttu-id="794f1-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="794f1-111">-Context</span></span>
<span data-ttu-id="794f1-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="794f1-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="794f1-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="794f1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="794f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794f1-114">-DefaultProfile</span></span>
<span data-ttu-id="794f1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="794f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="794f1-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="794f1-116">-UserId</span></span>
<span data-ttu-id="794f1-117">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="794f1-117">Specifies a user ID.</span></span>
<span data-ttu-id="794f1-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="794f1-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794f1-119">CommonParameters</span></span>
<span data-ttu-id="794f1-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="794f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794f1-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="794f1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794f1-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="794f1-122">INPUTS</span></span>

### <span data-ttu-id="794f1-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="794f1-123">None</span></span>
<span data-ttu-id="794f1-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="794f1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="794f1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="794f1-125">OUTPUTS</span></span>

### <span data-ttu-id="794f1-126">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="794f1-126">string</span></span>

## <span data-ttu-id="794f1-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="794f1-127">NOTES</span></span>

## <span data-ttu-id="794f1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="794f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="794f1-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="794f1-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


