---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: b9d7426bf275571d025ec0fef3f8bbec7c119c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503307"
---
# <span data-ttu-id="60405-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="60405-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="60405-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60405-102">SYNOPSIS</span></span>
<span data-ttu-id="60405-103">A konfigurációs adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="60405-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60405-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60405-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60405-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60405-105">DESCRIPTION</span></span>
<span data-ttu-id="60405-106">A **Get-AzureRmApiManagementTenantSyncState** parancsmag a beállítási adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="60405-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="60405-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60405-107">EXAMPLES</span></span>

### <span data-ttu-id="60405-108">Példa 1: a legutóbbi szinkronizálás állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="60405-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $ApimContext
```

<span data-ttu-id="60405-109">Ez a parancs a konfigurációs adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="60405-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="60405-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60405-110">PARAMETERS</span></span>

### <span data-ttu-id="60405-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="60405-111">-Context</span></span>
<span data-ttu-id="60405-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="60405-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="60405-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60405-113">-DefaultProfile</span></span>
<span data-ttu-id="60405-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60405-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60405-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60405-115">CommonParameters</span></span>
<span data-ttu-id="60405-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60405-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60405-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60405-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60405-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60405-118">INPUTS</span></span>

## <span data-ttu-id="60405-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60405-119">OUTPUTS</span></span>

### <span data-ttu-id="60405-120">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="60405-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="60405-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60405-121">NOTES</span></span>

## <span data-ttu-id="60405-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60405-122">RELATED LINKS</span></span>

