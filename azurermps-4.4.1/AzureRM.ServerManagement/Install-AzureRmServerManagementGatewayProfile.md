---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672690"
---
# <span data-ttu-id="09283-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="09283-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="09283-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09283-102">SYNOPSIS</span></span>
<span data-ttu-id="09283-103">Kiszolgálói felügyeleti átjáró-profil telepítése</span><span class="sxs-lookup"><span data-stu-id="09283-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09283-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09283-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09283-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09283-105">DESCRIPTION</span></span>
<span data-ttu-id="09283-106">A **telepítés-AzureRmServerManagementGatewayProfile** parancsmag a megfelelő helyre telepíti az Azure Server Management Gateway-profilt.</span><span class="sxs-lookup"><span data-stu-id="09283-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="09283-107">A parancsmag által telepített fájl neve profile.js.</span><span class="sxs-lookup"><span data-stu-id="09283-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="09283-108">Példák</span><span class="sxs-lookup"><span data-stu-id="09283-108">EXAMPLES</span></span>

## <span data-ttu-id="09283-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09283-109">PARAMETERS</span></span>

### <span data-ttu-id="09283-110">-InputFile</span><span class="sxs-lookup"><span data-stu-id="09283-110">-InputFile</span></span>
<span data-ttu-id="09283-111">Annak a helyi fájlnak a neve, amely a telepítendő átjáró profilt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="09283-111">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="09283-112">A parancsmag által telepített fájlt előzőleg az Save-AzureRmServerManagementGatewayProfile parancsmaggal kellett menteni.</span><span class="sxs-lookup"><span data-stu-id="09283-112">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09283-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09283-113">-DefaultProfile</span></span>
<span data-ttu-id="09283-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09283-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09283-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09283-115">CommonParameters</span></span>
<span data-ttu-id="09283-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09283-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09283-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09283-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09283-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09283-118">INPUTS</span></span>

### <span data-ttu-id="09283-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="09283-119">FileInfo</span></span>
<span data-ttu-id="09283-120">A ' InputFile ' paraméter az "FileInfo" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="09283-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="09283-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09283-121">OUTPUTS</span></span>

## <span data-ttu-id="09283-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09283-122">NOTES</span></span>

## <span data-ttu-id="09283-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09283-123">RELATED LINKS</span></span>

[<span data-ttu-id="09283-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="09283-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="09283-125">Mentés-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="09283-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


