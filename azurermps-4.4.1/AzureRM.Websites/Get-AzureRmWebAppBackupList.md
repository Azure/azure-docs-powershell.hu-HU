---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 02c83e79b5f56d4ef9a6d7730efb5cf5c42a9da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673071"
---
# <span data-ttu-id="9bb40-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="9bb40-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="9bb40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bb40-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb40-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bb40-103">SYNTAX</span></span>

### <span data-ttu-id="9bb40-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9bb40-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bb40-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9bb40-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bb40-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bb40-106">DESCRIPTION</span></span>
<span data-ttu-id="9bb40-107">A **Get-AzureRmWebAppBackupList** parancsmag az Azure Web App biztonsági másolatainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="9bb40-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="9bb40-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9bb40-108">EXAMPLES</span></span>

### <span data-ttu-id="9bb40-109">1:</span><span class="sxs-lookup"><span data-stu-id="9bb40-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="9bb40-110">Ez a parancs visszaad egy, az erőforráscsoport ContosoResourceGroup társított WebApp WebAppStandard vonatkozó biztonsági listát.</span><span class="sxs-lookup"><span data-stu-id="9bb40-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="9bb40-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bb40-111">PARAMETERS</span></span>

### <span data-ttu-id="9bb40-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9bb40-112">-Name</span></span>
<span data-ttu-id="9bb40-113">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="9bb40-113">WebApp Name</span></span>

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

### <span data-ttu-id="9bb40-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb40-114">-ResourceGroupName</span></span>
<span data-ttu-id="9bb40-115">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9bb40-115">Resource Group Name</span></span>

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

### <span data-ttu-id="9bb40-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="9bb40-116">-Slot</span></span>
<span data-ttu-id="9bb40-117">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="9bb40-117">Slot name</span></span>

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

### <span data-ttu-id="9bb40-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9bb40-118">-WebApp</span></span>
<span data-ttu-id="9bb40-119">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="9bb40-119">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb40-120">-DefaultProfile</span></span>
<span data-ttu-id="9bb40-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bb40-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bb40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb40-122">CommonParameters</span></span>
<span data-ttu-id="9bb40-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bb40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb40-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb40-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb40-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bb40-125">INPUTS</span></span>

### <span data-ttu-id="9bb40-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="9bb40-126">Site</span></span>
<span data-ttu-id="9bb40-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9bb40-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9bb40-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bb40-128">OUTPUTS</span></span>

### <span data-ttu-id="9bb40-129">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="9bb40-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="9bb40-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bb40-130">NOTES</span></span>

## <span data-ttu-id="9bb40-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bb40-131">RELATED LINKS</span></span>

