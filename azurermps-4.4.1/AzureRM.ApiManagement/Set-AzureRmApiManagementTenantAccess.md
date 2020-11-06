---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492591"
---
# <span data-ttu-id="8c9fe-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="8c9fe-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="8c9fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9fe-103">Engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c9fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c9fe-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c9fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c9fe-105">DESCRIPTION</span></span>
<span data-ttu-id="8c9fe-106">A **set-AzureRmApiManagementTenantAccess** parancsmag engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="8c9fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c9fe-107">EXAMPLES</span></span>

### <span data-ttu-id="8c9fe-108">1. példa: a bérlői hozzáférés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8c9fe-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="8c9fe-109">Ez a parancs engedélyezi a bérlői hozzáférést a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="8c9fe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c9fe-110">PARAMETERS</span></span>

### <span data-ttu-id="8c9fe-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8c9fe-111">-Context</span></span>
<span data-ttu-id="8c9fe-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8c9fe-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8c9fe-113">-Enabled</span></span>
<span data-ttu-id="8c9fe-114">Megadja, hogy ez a parancsmag engedélyezi vagy tiltja-e a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="8c9fe-115">Adja meg a letiltáshoz vagy az $False engedélyezéséhez $True értékét.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-115">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9fe-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c9fe-116">-PassThru</span></span>
<span data-ttu-id="8c9fe-117">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementAccessInformation** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8c9fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9fe-118">-DefaultProfile</span></span>
<span data-ttu-id="8c9fe-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c9fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c9fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9fe-120">CommonParameters</span></span>
<span data-ttu-id="8c9fe-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c9fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9fe-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c9fe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9fe-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c9fe-123">INPUTS</span></span>

## <span data-ttu-id="8c9fe-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c9fe-124">OUTPUTS</span></span>

### <span data-ttu-id="8c9fe-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="8c9fe-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="8c9fe-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c9fe-126">NOTES</span></span>

## <span data-ttu-id="8c9fe-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c9fe-127">RELATED LINKS</span></span>

[<span data-ttu-id="8c9fe-128">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="8c9fe-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


