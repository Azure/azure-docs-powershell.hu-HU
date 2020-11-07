---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679297"
---
# <span data-ttu-id="f1e83-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="f1e83-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="f1e83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1e83-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e83-103">A pince hitelesítő adatait tartalmazó fájl letöltése a biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="f1e83-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1e83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1e83-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1e83-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1e83-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e83-106">A **Get-AzureRmBackupVaultCredentials** parancsmag letölti a Vault hitelesítő adatait tartalmazó fájlt az Azure Backup Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="f1e83-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="f1e83-107">Biztonsági másolat: egy kiszolgáló csatlakoztatása az Azure Backup Vault-hoz, és regisztrálja a kiszolgálóját a boltozat hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="f1e83-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="f1e83-108">Ahhoz, hogy biztonsági másolatot küldene a boltozatról, regisztrálnia kell a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="f1e83-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="f1e83-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f1e83-109">EXAMPLES</span></span>

## <span data-ttu-id="f1e83-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1e83-110">PARAMETERS</span></span>

### <span data-ttu-id="f1e83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e83-111">-DefaultProfile</span></span>
<span data-ttu-id="f1e83-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1e83-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1e83-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="f1e83-113">-TargetLocation</span></span>
<span data-ttu-id="f1e83-114">A cél elérési útvonalát adja meg, ahol ez a parancsmag tárolja a Vault hitelesítő adatait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="f1e83-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e83-115">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="f1e83-115">-Vault</span></span>
<span data-ttu-id="f1e83-116">Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag a Vault-hitelesítőadat-fájlt kapja.</span><span class="sxs-lookup"><span data-stu-id="f1e83-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="f1e83-117">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f1e83-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e83-118">CommonParameters</span></span>
<span data-ttu-id="f1e83-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1e83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e83-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e83-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e83-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e83-121">INPUTS</span></span>

### <span data-ttu-id="f1e83-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="f1e83-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="f1e83-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e83-123">OUTPUTS</span></span>

### <span data-ttu-id="f1e83-124">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f1e83-124">String</span></span>
<span data-ttu-id="f1e83-125">Ez a parancsmag a Vault hitelesítőadat-fájl nevét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f1e83-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="f1e83-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1e83-126">NOTES</span></span>

## <span data-ttu-id="f1e83-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1e83-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1e83-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f1e83-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


