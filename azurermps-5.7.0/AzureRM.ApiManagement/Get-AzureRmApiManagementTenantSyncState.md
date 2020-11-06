---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: 64e1d8ad070d4ce1c2f8129a73efd8730f26d1a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495492"
---
# <span data-ttu-id="a53dd-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="a53dd-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="a53dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a53dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a53dd-103">A konfigurációs adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a53dd-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a53dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a53dd-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a53dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a53dd-105">DESCRIPTION</span></span>
<span data-ttu-id="a53dd-106">A **Get-AzureRmApiManagementTenantSyncState** parancsmag a beállítási adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a53dd-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="a53dd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a53dd-107">EXAMPLES</span></span>

### <span data-ttu-id="a53dd-108">Példa 1: a legutóbbi szinkronizálás állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a53dd-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext 
```

<span data-ttu-id="a53dd-109">Ez a parancs a konfigurációs adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a53dd-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="a53dd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a53dd-110">PARAMETERS</span></span>

### <span data-ttu-id="a53dd-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a53dd-111">-Context</span></span>
<span data-ttu-id="a53dd-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a53dd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a53dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a53dd-113">-DefaultProfile</span></span>
<span data-ttu-id="a53dd-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a53dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a53dd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53dd-115">CommonParameters</span></span>
<span data-ttu-id="a53dd-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a53dd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53dd-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a53dd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53dd-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a53dd-118">INPUTS</span></span>

### <span data-ttu-id="a53dd-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="a53dd-119">None</span></span>
<span data-ttu-id="a53dd-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a53dd-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a53dd-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a53dd-121">OUTPUTS</span></span>

### <span data-ttu-id="a53dd-122">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="a53dd-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="a53dd-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a53dd-123">NOTES</span></span>

## <span data-ttu-id="a53dd-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a53dd-124">RELATED LINKS</span></span>

