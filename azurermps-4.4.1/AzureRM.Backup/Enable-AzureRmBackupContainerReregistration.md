---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 1c89db6267fffeb73820150d1c73c3225f45cde2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493582"
---
# <span data-ttu-id="b3d14-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="b3d14-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="b3d14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3d14-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d14-103">Visszaregisztrálja a kiszolgálót, hogy egy biztonságimásolat-tárolóhoz csatlakozzon.</span><span class="sxs-lookup"><span data-stu-id="b3d14-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3d14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3d14-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3d14-105">DESCRIPTION</span></span>
<span data-ttu-id="b3d14-106">Az **enable-AzureRmBackupContainerReregistration** parancsmag újra regisztrálja a kiszolgálót az Azure Backup-tárolóhoz való csatlakozáshoz, és folytatja a biztonsági másolat helyreállítási pontjának a folytatását.</span><span class="sxs-lookup"><span data-stu-id="b3d14-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>

<span data-ttu-id="b3d14-107">Ha elpusztít egy szervert, az összes Felhőbeli biztonságimásolat-pontja a biztonsági másolatban marad.</span><span class="sxs-lookup"><span data-stu-id="b3d14-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="b3d14-108">Ha helyettesítő kiszolgálót hoz létre, és ugyanazt a teljesen minősített tartománynevet rendeli hozzá, a kiszolgálót visszakapcsolhatja ugyanahhoz a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="b3d14-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="b3d14-109">Ez a parancsmag lehetővé teszi biztonsági másolatok készítését és új biztonsági pontok hozzáadását a meglévő halmazhoz.</span><span class="sxs-lookup"><span data-stu-id="b3d14-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="b3d14-110">Az új kiszolgáló továbbra is a biztonsági mentési láncban marad.</span><span class="sxs-lookup"><span data-stu-id="b3d14-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="b3d14-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b3d14-111">EXAMPLES</span></span>

## <span data-ttu-id="b3d14-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3d14-112">PARAMETERS</span></span>

### <span data-ttu-id="b3d14-113">-Container</span><span class="sxs-lookup"><span data-stu-id="b3d14-113">-Container</span></span>
<span data-ttu-id="b3d14-114">Azt a tárolót adja meg, amelyre a parancsmag újra regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="b3d14-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="b3d14-115">Ha **AzureRmBackupContainer** szeretne beolvasni, használja az Get-AzureRmBackupContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b3d14-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d14-116">-DefaultProfile</span></span>
<span data-ttu-id="b3d14-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3d14-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3d14-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d14-118">CommonParameters</span></span>
<span data-ttu-id="b3d14-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3d14-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d14-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3d14-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d14-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3d14-121">INPUTS</span></span>

### <span data-ttu-id="b3d14-122">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b3d14-122">AzureBackupContainer</span></span>

## <span data-ttu-id="b3d14-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3d14-123">OUTPUTS</span></span>

### <span data-ttu-id="b3d14-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="b3d14-124">None</span></span>

## <span data-ttu-id="b3d14-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3d14-125">NOTES</span></span>

## <span data-ttu-id="b3d14-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3d14-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3d14-127">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b3d14-127">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b3d14-128">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b3d14-128">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


