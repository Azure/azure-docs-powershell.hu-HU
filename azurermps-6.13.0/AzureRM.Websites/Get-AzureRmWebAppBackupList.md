---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: f4005df31746b63b2a45fa2c78f254e2d5f24c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492662"
---
# <span data-ttu-id="18815-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="18815-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="18815-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18815-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18815-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18815-103">SYNTAX</span></span>

### <span data-ttu-id="18815-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="18815-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18815-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="18815-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18815-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="18815-106">DESCRIPTION</span></span>
<span data-ttu-id="18815-107">A **Get-AzureRmWebAppBackupList** parancsmag az Azure Web App biztonsági másolatainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="18815-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="18815-108">Példák</span><span class="sxs-lookup"><span data-stu-id="18815-108">EXAMPLES</span></span>

### <span data-ttu-id="18815-109">1:</span><span class="sxs-lookup"><span data-stu-id="18815-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="18815-110">Ez a parancs visszaad egy, az erőforráscsoport ContosoResourceGroup társított WebApp WebAppStandard vonatkozó biztonsági listát.</span><span class="sxs-lookup"><span data-stu-id="18815-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="18815-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18815-111">PARAMETERS</span></span>

### <span data-ttu-id="18815-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18815-112">-DefaultProfile</span></span>
<span data-ttu-id="18815-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18815-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18815-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18815-114">-Name</span></span>
<span data-ttu-id="18815-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="18815-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18815-116">-ResourceGroupName</span></span>
<span data-ttu-id="18815-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="18815-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="18815-118">-Slot</span></span>
<span data-ttu-id="18815-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="18815-119">Slot name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="18815-120">-WebApp</span></span>
<span data-ttu-id="18815-121">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="18815-121">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18815-122">CommonParameters</span></span>
<span data-ttu-id="18815-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18815-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18815-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18815-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18815-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18815-125">INPUTS</span></span>

### <span data-ttu-id="18815-126">System. String</span><span class="sxs-lookup"><span data-stu-id="18815-126">System.String</span></span>

### <span data-ttu-id="18815-127">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="18815-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="18815-128">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="18815-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="18815-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18815-129">OUTPUTS</span></span>

### <span data-ttu-id="18815-130">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="18815-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="18815-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18815-131">NOTES</span></span>

## <span data-ttu-id="18815-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18815-132">RELATED LINKS</span></span>
