---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 057bebde5eada143c9ee00260a1406fdceae9436
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842790"
---
# <span data-ttu-id="b2d8f-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="b2d8f-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="b2d8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2d8f-102">SYNOPSIS</span></span>

## <span data-ttu-id="b2d8f-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2d8f-103">SYNTAX</span></span>

### <span data-ttu-id="b2d8f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b2d8f-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d8f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b2d8f-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2d8f-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2d8f-106">DESCRIPTION</span></span>
<span data-ttu-id="b2d8f-107">A **Get-AzWebAppBackupList** parancsmag az Azure Web App biztonsági másolatainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="b2d8f-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="b2d8f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b2d8f-108">EXAMPLES</span></span>

### <span data-ttu-id="b2d8f-109">1:</span><span class="sxs-lookup"><span data-stu-id="b2d8f-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="b2d8f-110">Ez a parancs visszaad egy, az erőforráscsoport ContosoResourceGroup társított WebApp WebAppStandard vonatkozó biztonsági listát.</span><span class="sxs-lookup"><span data-stu-id="b2d8f-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="b2d8f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2d8f-111">PARAMETERS</span></span>

### <span data-ttu-id="b2d8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d8f-112">-DefaultProfile</span></span>
<span data-ttu-id="b2d8f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2d8f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d8f-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2d8f-114">-Name</span></span>
<span data-ttu-id="b2d8f-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="b2d8f-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d8f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d8f-116">-ResourceGroupName</span></span>
<span data-ttu-id="b2d8f-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b2d8f-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d8f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2d8f-118">-Slot</span></span>
<span data-ttu-id="b2d8f-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="b2d8f-119">Slot name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d8f-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b2d8f-120">-WebApp</span></span>
<span data-ttu-id="b2d8f-121">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="b2d8f-121">Piped WebApp</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d8f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d8f-122">CommonParameters</span></span>
<span data-ttu-id="b2d8f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2d8f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d8f-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d8f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d8f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2d8f-125">INPUTS</span></span>

### <span data-ttu-id="b2d8f-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="b2d8f-126">Site</span></span>
<span data-ttu-id="b2d8f-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b2d8f-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b2d8f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2d8f-128">OUTPUTS</span></span>

### <span data-ttu-id="b2d8f-129">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="b2d8f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="b2d8f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2d8f-130">NOTES</span></span>

## <span data-ttu-id="b2d8f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2d8f-131">RELATED LINKS</span></span>

