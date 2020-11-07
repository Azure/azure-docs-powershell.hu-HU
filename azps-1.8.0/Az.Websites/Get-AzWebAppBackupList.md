---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: fab8973c63e419cdef45fb79a0ad5182c46f2de5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668364"
---
# <span data-ttu-id="fc139-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="fc139-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="fc139-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc139-102">SYNOPSIS</span></span>

## <span data-ttu-id="fc139-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc139-103">SYNTAX</span></span>

### <span data-ttu-id="fc139-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fc139-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc139-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fc139-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc139-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc139-106">DESCRIPTION</span></span>
<span data-ttu-id="fc139-107">A **Get-AzWebAppBackupList** parancsmag az Azure Web App biztonsági másolatainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="fc139-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="fc139-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fc139-108">EXAMPLES</span></span>

### <span data-ttu-id="fc139-109">1:</span><span class="sxs-lookup"><span data-stu-id="fc139-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="fc139-110">Ez a parancs visszaad egy, az erőforráscsoport ContosoResourceGroup társított WebApp WebAppStandard vonatkozó biztonsági listát.</span><span class="sxs-lookup"><span data-stu-id="fc139-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="fc139-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc139-111">PARAMETERS</span></span>

### <span data-ttu-id="fc139-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc139-112">-DefaultProfile</span></span>
<span data-ttu-id="fc139-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc139-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc139-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc139-114">-Name</span></span>
<span data-ttu-id="fc139-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="fc139-115">WebApp Name</span></span>

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

### <span data-ttu-id="fc139-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc139-116">-ResourceGroupName</span></span>
<span data-ttu-id="fc139-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fc139-117">Resource Group Name</span></span>

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

### <span data-ttu-id="fc139-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="fc139-118">-Slot</span></span>
<span data-ttu-id="fc139-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="fc139-119">Slot name</span></span>

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

### <span data-ttu-id="fc139-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fc139-120">-WebApp</span></span>
<span data-ttu-id="fc139-121">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="fc139-121">Piped WebApp</span></span>

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

### <span data-ttu-id="fc139-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc139-122">CommonParameters</span></span>
<span data-ttu-id="fc139-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc139-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc139-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc139-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc139-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc139-125">INPUTS</span></span>

### <span data-ttu-id="fc139-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fc139-126">System.String</span></span>

### <span data-ttu-id="fc139-127">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="fc139-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fc139-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc139-128">OUTPUTS</span></span>

### <span data-ttu-id="fc139-129">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="fc139-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="fc139-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc139-130">NOTES</span></span>

## <span data-ttu-id="fc139-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc139-131">RELATED LINKS</span></span>
