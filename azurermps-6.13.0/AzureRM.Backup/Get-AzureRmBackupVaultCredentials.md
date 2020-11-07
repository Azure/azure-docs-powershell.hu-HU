---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: 6ee9e3062108049e517dbea09573af7905dd54d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679183"
---
# <span data-ttu-id="083ee-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="083ee-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="083ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="083ee-102">SYNOPSIS</span></span>
<span data-ttu-id="083ee-103">A pince hitelesítő adatait tartalmazó fájl letöltése a biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="083ee-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="083ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="083ee-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="083ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="083ee-105">DESCRIPTION</span></span>
<span data-ttu-id="083ee-106">A **Get-AzureRmBackupVaultCredentials** parancsmag letölti a Vault hitelesítő adatait tartalmazó fájlt az Azure Backup Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="083ee-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>
<span data-ttu-id="083ee-107">Biztonsági másolat: egy kiszolgáló csatlakoztatása az Azure Backup Vault-hoz, és regisztrálja a kiszolgálóját a boltozat hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="083ee-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="083ee-108">Ahhoz, hogy biztonsági másolatot küldene a boltozatról, regisztrálnia kell a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="083ee-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="083ee-109">Példák</span><span class="sxs-lookup"><span data-stu-id="083ee-109">EXAMPLES</span></span>

## <span data-ttu-id="083ee-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="083ee-110">PARAMETERS</span></span>

### <span data-ttu-id="083ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083ee-111">-DefaultProfile</span></span>
<span data-ttu-id="083ee-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="083ee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="083ee-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="083ee-113">-TargetLocation</span></span>
<span data-ttu-id="083ee-114">A cél elérési útvonalát adja meg, ahol ez a parancsmag tárolja a Vault hitelesítő adatait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="083ee-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083ee-115">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="083ee-115">-Vault</span></span>
<span data-ttu-id="083ee-116">Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag a Vault-hitelesítőadat-fájlt kapja.</span><span class="sxs-lookup"><span data-stu-id="083ee-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="083ee-117">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="083ee-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="083ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083ee-118">CommonParameters</span></span>
<span data-ttu-id="083ee-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="083ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083ee-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083ee-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083ee-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="083ee-121">INPUTS</span></span>

### <span data-ttu-id="083ee-122">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="083ee-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="083ee-123">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="083ee-123">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="083ee-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="083ee-124">OUTPUTS</span></span>

### <span data-ttu-id="083ee-125">System. String</span><span class="sxs-lookup"><span data-stu-id="083ee-125">System.String</span></span>
<span data-ttu-id="083ee-126">Ez a parancsmag a Vault hitelesítőadat-fájl nevét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="083ee-126">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="083ee-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="083ee-127">NOTES</span></span>

## <span data-ttu-id="083ee-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="083ee-128">RELATED LINKS</span></span>

[<span data-ttu-id="083ee-129">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="083ee-129">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


